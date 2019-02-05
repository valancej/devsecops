# What is DevSecOps?

Here at Anchore, we consistently work with our users and customers to improve the security of their container images. During these conversations, there is typically an initiative to embed container image scanning into CI/CD pipelines to meet **__DevSecOps__** goals. But what do we mean when we say **__DevSecOps__**? We can think of **__DevSecOps__** as empowering engineering teams to take ownership of how their products will perform in production by integrating security practices into their existing automation and DevOps workflow. A core principle of DevSecOps is creating a 'Security as Code' culture. Now that's there is increased transparency and collaboration, security is now everyone's responsibility. By building on the cultural changes of the DevOps framework, security teams are added to DevOps initiatives early to help plan for security automation. Additionally, security engineers should constantly be providing feedback and educating both Ops and development teams on best practices.

## What are the benefits of DevSecOps?

There are quite a few benefits to including security practices to the software development and delivery lifecycle. I've listed some of the core benefits below:

- Costs are reduced by uncovering and fixing security issues further left in the development lifecycle versus in production environments.
- Speed of product delivery is increased by incorporating automated security tests versus adding security testing at the end of lifecycle.
- Increased transparency and team collaboration leads to faster detection and recovery of threats. 
- Implementing immutable infrastructure improves overall security by reducing vulnerabilities, increasing automation, and encourages organizations to move to the cloud. 

When thinking about what tooling and tests to put in place, organizations should look at their entire development lifecycle and environment. This can often include,source control, third-party libraries, container registries, CI/CD pipelines, and orchestration and release tools. 

## Anchore and DevSecOps

As a container security company, we strongly believe containers help with a successful journey to DevSecOps. Containers are lightweight, faster than VMs, and allow developers to create predictable, scalable environments isolated from other applications or services. This leads to increased productivity across all teams, faster development, and less time fixing bugs and other environment issues. Containers are also immutable, meaning unchanged once created. To fix a vulnerable container, it is simply replaced by a patched, newer version.

When planning security steps in a continuous integration pipeline, I often recommend adding a mandatory image analysis step to uncover vulnerable packages, secrets, credentials, or misconfigurations prior to the image being pushed to a production registry. As part of this image scanning step I also recommend enforcing policies on the contents of the container images that have just been analyzed. Anchore policies are made up of a set of user-defined rules such as:

- Security vulnerabilities
- Image manifest changes
- Configuration file contents
- Presence of credentials in an image
- Unused exposed ports
- Package whitelists and blacklists

Based on the rules created and the final result of the policy evaluation, users can choose to fail the image scanning step of a CI build, and not promote the image to a production container registry. The integration of a flexible policy engine helps organizations stay on top of compliance requirements constantly and can react faster if audited. Security teams responsible creating policy rules should be educating developers on why these rules are being created and what steps they can take to avoid breaking them.

## Conclusion

DevSecOps means integrating security practices into application development from start to finish. Not only does this require new tooling, automation, and integration, but it also involves a significant culture change and investment from every developer, release engineer, and security engineer. Everyone is responsible for openness, feedback, and education. Once the culture is intact an in place, DevSecOps practices and processes can be implemented to achieve a more secure development process as a whole.