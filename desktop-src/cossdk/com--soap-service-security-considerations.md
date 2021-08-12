---
description: Considerações sobre segurança do serviço SOAP COM+
ms.assetid: c4f7744c-ff57-4d9d-8632-7e5bbb73449a
title: Considerações sobre segurança do serviço SOAP COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c67e034dfeaa4ec7f8688420aafcaec434653c942665ec3e3cbaa1535b51980d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118548545"
---
# <a name="com-soap-service-security-considerations"></a>Considerações sobre segurança do serviço SOAP COM+

O serviço SOAP COM+ depende do servidor Web do IIS para segurança. Mesmo no [modo de](accessing-xml-web-services-in-cao-mode.md)objeto ativado pelo cliente, um RPC COM+ não transmite a identidade do cliente e, portanto, não pode usar a segurança baseada em função ou qualquer outro recurso de segurança fornecido pelo DCOM. Se você quiser ajudar a proteger a privacidade dos dados transmitidos de e para seu serviço Web XML ou para ajudar a proteger seu serviço Web XML contra acesso não autorizado, você pode configurar o IIS para limitar o acesso a um serviço Web XML com base em um endereço IP de clientes ou exigir que um cliente apresente um certificado digital para verificar sua identidade. Se você não limitar o acesso, qualquer cliente que possa se comunicar com seu servidor Web poderá acessar seu serviço Web XML.

Você pode configurar o IIS para criptografar suas comunicações de serviço Web XML com clientes usando protocolos SSL ou TLS de criptografia de chave pública. Se você não criptografar as comunicações SOAP, os dados trocados entre um cliente e um servidor poderão ser observados por terceiros com acesso a qualquer rede pela qual a comunicação SOAP percorre; dependendo da topologia de rede, isso pode ser uma LAN pequena ou pode ser a Internet.

Por padrão, as comunicações SOAP não criptografadas são recebidas na porta HTTP (80) e as comunicações SOAP criptografadas são recebidas na porta HTTPS (443). Para que um cliente acesse com êxito um serviço Web XML, todos os firewalls entre o cliente e o servidor devem ser configurados para permitir que os pacotes TCP SYN atinjam a porta de servidor apropriada. Por outro lado, para limitar o acesso aos serviços Web XML, um administrador de firewall pode optar por fechar essas portas.

As configurações de segurança padrão para um componente COM exposto como um serviço Web XML diferem dependendo de qual versão do Microsoft .NET Framework está instalada. Se a versão 1.0 estiver instalada, os serviços Web XML não serão securso por padrão; todas as chamadas são aceitas e nenhuma criptografia é usada. Se a versão 1.1 ou posterior estiver instalada, os serviços Web XML serão seguros por padrão; os chamadores devem ser autenticados e a criptografia é necessária.

Um serviço Web XML seguro não dá suporte ao acesso WKO via WSDL. Em vez disso, os clientes que instalaram o .NET Framework versão 1.1 podem chamá-lo no modo DEEI. Se clientes de terceiros precisam acessar seu serviço Web XML por meio do WSDL, você deve permitir o acesso anônimo.

Um componente COM exposto como um serviço Web XML é executado por padrão com as permissões do usuário anônimo (não com as permissões de seu chamador). Você pode configurar o IIS para executar o serviço Web XML como um usuário diferente; Às vezes, isso pode ser necessário porque o componente usa arquivos ou outros recursos aos quais o usuário anônimo não tem acesso. No entanto, você sempre deve tentar executar seu componente com o menor número de privilégios possíveis, para limitar o dano que um chamador mal-intencionado pode causar.

> [!Note]  
> Como um método exposto por meio de um serviço Web XML pode potencialmente ser exposto a chamadores mal-intencionados, você sempre deve validar os parâmetros de entrada dos quais ele depende.

 

Para obter instruções detalhadas sobre como definir configurações específicas de segurança do serviço Web XML, consulte [Proteger serviços Web XML.](securing-xml-web-services.md)

**Para converter um aplicativo SOAP seguro em um aplicativo SOAP não seguro**

1.  Abra a ferramenta de administração Serviços de Informações da Internet (IIS).
2.  Localize o diretório virtual do aplicativo e abra a **caixa de diálogo** Propriedades.
3.  Marque **a página Habilitar conteúdo** padrão na **guia** Documentos.
4.  Na guia **Segurança de Diretório,** clique em **Editar em** Acesso anônimo e controle **de autenticação**.
5.  Marque **Acesso anônimo para** habilitar o acesso anônimo e clique em **OK.**
6.  Clique **em Editar** em **Comunicações seguras.**
7.  Desmarque a caixa de seleção Exigir canal seguro **(SSL).**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão geral do serviço COM+ SOAP](com--soap-service-overview.md)
</dt> </dl>

 

 



