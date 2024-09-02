# aws-self-hosted-url-shortener

## Infrastructure Diagram

![Infrastructure Diagram](https://cdn.silverlining.cloud/cloudformation-url-shortener/aws-self-hosted-url-shortener-github.png)

## Deployment

1. **Install the AWS CLI**: To deploy this CloudFormation stack, you need to have the AWS CLI installed. Follow the [AWS CLI installation guide](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) for instructions.

2. **Download the Template**: Download the `template.yaml` file from this repository.

3. **Upload the Template to S3**: Since the template is large, AWS requires it to be uploaded to an S3 bucket before deployment. Use the following command to upload it:

    ```bash
    aws s3 cp template.yaml s3://<YOUR_BUCKET_NAME>/templates/template.yaml
    ```

4. **Deploy the Stack**: Run the following command to deploy the stack using CloudFormation:

    ```bash
    aws cloudformation create-stack --stack-name <STACK_NAME> --template-url https://<YOUR_BUCKET_NAME>.s3.amazonaws.com/templates/template.yaml --capabilities CAPABILITY_NAMED_IAM --region <REGION>
    ```

**Demo Deployment**

You can explore a demo deployment of the paid commercial version at [self.aws3-demo.link](https://self.aws3-demo.link). Use the following API key to access it:

**API Key**: `7DRpNbuO5e8Tk37WiJmjB4ILH8kkYcOF7l6eldD5`

## Commercial Version

### Paid Version

In addition to our free Infrastructure-as-a-Service (IaaS) stack, we offer a paid version that includes enhanced features such as:

- **Custom URL Slug Modification**: Personalize your links for better branding and recognition.
- **Link Expiration**: Set links to expire after a certain time or after a specified number of clicks.
- **Click Tracking**: Monitor who clicked your links and when they were clicked.

Purchase our paid version directly from the AWS Marketplace and deploy it: [AWS Marketplace - Paid Version](https://aws.amazon.com/marketplace/pp/prodview-y3fqwgluejol6)

### Software as a Service (SaaS)

Avoid the hassle of hosting by using our SaaS URL Shortener service. Our fully Pay-As-You-Go pricing model ensures you only pay for what you use, at just **USD 0.004 per shortened link**. There are no additional costs for contracts or link traffic.

Subscribe now: [AWS Marketplace - SaaS URL Shortener](https://aws.amazon.com/marketplace/pp/prodview-aduakv5eklenq)

## Feature Comparision

| Feature                                           | Free IaaS | Paid IaaS | SaaS |
|---------------------------------------------------|:---------:|:---------:|:----:|
| **Generate short links through API and website**  <br> Easily create short, shareable links using API or through a website interface. |     ✔     |     ✔     |  ✔   |
| **Remove and List existing short links**          <br> Manage your links efficiently with options to delete and view all your short links. |     ✔     |     ✔     |  ✔   |
| **Serverless infrastructure**                     <br> Leverage scalable and flexible serverless technology for efficient link management. |     ✔     |     ✔     |  ✔   |
| **Connect your own (sub-)domain**                 <br> Enhance your branding by using a custom (sub-)domain for your short links. |     ✔     |     ✔     |  ✔   |
| **Secured by API key**                            <br> Keep your link generation and management secure with API key authentication. |     ✔     |     ✔     |  ✔   |
| **Track link clicks**                             <br> Gain insights by tracking how often and by whom links were clicked. |           |     ✔     |  ✔   |
| **Short URL customization**                       <br> Create personalized short URLs by customizing the URL slugs or adjusting the slug length, making your links more memorable and aligned with your brand identity. |           |     ✔     |  ✔   |
| **Link expiration by time and clicks**            <br> Set expiration rules for your links based on time duration or click limits. |           |     ✔     |  ✔   |
| **Commercial Use**                                <br> Ideal for businesses with advanced needs, supporting commercial use of short links. |           |     ✔     |  ✔   |
| **Support via live chat and email**               <br> Get prompt help and support through live chat and email, ensuring smooth operations. |           |     ✔     |  ✔   |
| **No infrastructure setup required**              <br> Simplify operations with no need to manage infrastructure; we handle it all. |           |           |  ✔   |
| **Pay-as-you-go pricing**                         <br> Only pay for the links you create, with no additional costs, offering a cost-effective solution. |           |           |  ✔   |




## License

This CloudFormation template is made available under a dual-license. You can use this free template, licensed under the GPL-3.0 license, to integrate the URL Shortener into your open-source, non-commercial project. If you want to use this CloudFormation template in a closed-source and/or commercial project, you will need to purchase our paid version [here](https://aws.amazon.com/marketplace/pp/prodview-y3fqwgluejol6).

By purchasing a commercial license, you not only gain access to all features and enterprise-level support, either via our live chat on our website or via email, but you also support the future development of this project.
