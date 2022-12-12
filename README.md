# terraform-variablesh
h
provider "aws"{
    region     = "ap-south-1"
    access_key = "AKIAX4C22QF3B4623Y5I"
    secret_key = "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"
}


resource "aws_instance" "abb"{
    ami           = "ami-03e335a55ff214da0"
    instance_type = var.instance_type
    
    tags = {

          name = "abb"
    }    
}

variable "instance_type" {
    description = "instance type t2.micro"
    type        = string
    default     = "t2.micro"
}
