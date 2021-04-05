---
description: Considerações de segurança do serviço SOAP COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Considerações de segurança do serviço SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a238860e154e9928672a64ef44f9db37e9c8ad2c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826647"
---
# <a name="com-soap-service-security-considerations"></a>Considerações de segurança do serviço SOAP COM+

O serviço SOAP COM+ depende do servidor Web do IIS para segurança. Mesmo no [modo de objeto ativado pelo cliente](accessing-xml-web-services-in-cao-mode.md), um RPC do com+ não transmite a identidade do cliente e, portanto, não pode usar a segurança baseada em função ou qualquer outro recurso de segurança fornecido pelo DCOM. Se você quiser ajudar a proteger a privacidade dos dados transmitidos de e para o serviço Web XML, ou para ajudar a proteger seu serviço Web XML contra acesso não autorizado, você pode configurar o IIS para limitar o acesso a um serviço Web XML com base em um endereço IP de clientes ou para exigir que um cliente apresente um certificado digital para verificar sua identidade. Se você não limitar o acesso, qualquer cliente que possa se comunicar com o servidor Web poderá acessar o serviço Web XML.

Você pode configurar o IIS para criptografar suas comunicações de serviço Web XML com clientes usando protocolos TLS ou SSL de criptografia de chave pública. Se você não criptografar comunicações SOAP, os dados trocados entre um cliente e um servidor poderão ser observados por terceiros com acesso a qualquer rede sobre a qual a comunicação SOAP viaja; dependendo da topologia de rede, essa pode ser uma rede local pequena ou pode ser a Internet.

Por padrão, as comunicações SOAP não criptografadas são recebidas na porta HTTP (80) e as comunicações SOAP criptografadas são recebidas na porta HTTPS (443). Para que um cliente acesse com êxito um serviço Web XML, todos os firewalls entre o cliente e o servidor devem ser configurados para permitir que os pacotes TCP SYN alcancem a porta do servidor apropriada. Por outro lado, para limitar o acesso a serviços Web XML, um administrador de firewall pode optar por fechar essas portas.

As configurações de segurança padrão para um componente COM exposto como um serviço Web XML diferem dependendo de qual versão do Microsoft .NET Framework está instalada. Se a versão 1,0 estiver instalada, os serviços Web XML não serão seguros por padrão; todas as chamadas são aceitas e nenhuma criptografia é usada. Se a versão 1,1 ou posterior estiver instalada, os serviços Web XML serão protegidos por padrão; os chamadores devem ser autenticados e a criptografia é necessária.

Um serviço Web XML seguro não dá suporte ao acesso WKO via WSDL. Em vez disso, os clientes que instalaram a versão 1,1 do .NET Framework podem chamá-lo no modo CAO. Se os clientes de terceiros precisarem acessar o serviço Web XML via WSDL, você deverá permitir o acesso anônimo.

Um componente COM exposto como um serviço Web XML é executado por padrão com as permissões do usuário anônimo (não com as permissões de seu chamador). Você pode configurar o IIS para executar o serviço Web XML como um usuário diferente; às vezes, isso pode ser necessário porque o componente usa arquivos ou outros recursos aos quais o usuário anônimo não tem acesso. No entanto, você sempre deve tentar executar o componente com o menor privilégio possível, para limitar os danos que um chamador mal-intencionado pode causar.

> [!Note]  
> Como um método exposto por meio de um serviço Web XML pode ser exposto a chamadores mal-intencionados, você deve sempre certificar-se de validar todos os parâmetros de entrada dos quais ele depende.

 

Para obter instruções detalhadas sobre como definir configurações específicas de segurança de serviço Web XML, consulte [protegendo serviços Web XML](securing-xml-web-services.md).

**Para converter um aplicativo SOAP seguro em um aplicativo SOAP não seguro**

1.  Abra a ferramenta de administração do Serviços de Informações da Internet (IIS).
2.  Localize o diretório virtual do aplicativo e abra a caixa de diálogo **Propriedades** .
3.  Marque a **página habilitar conteúdo padrão** na guia **documentos** .
4.  Na guia **segurança de diretório** , clique em **Editar** em **acesso anônimo e controle de autenticação**.
5.  Marque **acesso anônimo** para habilitar o acesso anônimo e clique em **OK**.
6.  Clique em **Editar** em **comunicações seguras**.
7.  Desmarque a caixa de seleção **exigir canal de segurança (SSL)** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço SOAP COM+](com--soap-service-overview.md)
</dt> </dl>

 

 



