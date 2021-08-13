---
description: O acesso a aplicativos COM+ expostos como serviços Web XML é controlado pelo servidor Web do IIS, que processa as solicitações de entrada.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Proteger serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bccc49a096def7fdca3f508ca590cd23df0fbf2e92fd816ba55300931122361e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546959"
---
# <a name="securing-xml-web-services"></a>Proteger serviços Web XML

O acesso a aplicativos COM+ expostos como serviços Web XML é controlado pelo servidor Web do IIS, que processa as solicitações de entrada. Você também pode configurar o IIS para exigir que as comunicações com o chamador ocorrem em um canal seguro estabelecido usando o protocolo protocolo SSL (SSL).

> [!Note]  
> Um serviço Web XML seguro não dá suporte ao acesso WKO via WSDL. Em vez disso, os clientes que instalaram o .NET Framework versão 1.1 podem chamá-lo no modo DEEI. Se clientes de terceiros precisam acessar seu serviço Web XML por meio do WSDL, você deve permitir o acesso anônimo.

 

> [!Note]  
> Para usar o protocolo SSL para estabelecer um canal de comunicação seguro, você deve obter e instalar um certificado SSL.

 

## <a name="component-services-administrative-tool"></a>Ferramenta Administrativa dos Serviços de Componentes

Para selecionar o mecanismo de autenticação para um serviço Web XML, use as seguintes etapas:

1.  Clique com o botão direito **do Meu Computador** ícone na área de trabalho e clique em **Gerenciar**.

2.  Em **Serviços e Aplicativos e** Serviço de Informações da **Internet**, localize o ícone correspondente ao diretório raiz virtual do serviço Web XML. Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.

3.  Na guia **Segurança de** Diretório da caixa de diálogo propriedades, localize **Autenticação** e controle de acesso e clique no **botão Editar** correspondente.

4.  Na caixa **de diálogo Métodos de** Autenticação, em **Acesso** autenticado, use as caixas de seleção para selecionar os mecanismos de autenticação que você deseja permitir. Clique em **OK**.

    > [!Note]  
    > Você pode configurar o IIS para autenticar chamadores usando qualquer uma das seguintes opções na caixa de diálogo Métodos de Autenticação do **IIS:** Autenticação **integrada do Windows,** autenticação digest para servidores de domínio **do Windows,** Autenticação básica (a senha é enviada em texto não **claro)** ou autenticação do **.NET Passport**. Você também pode permitir o acesso anônimo.

     

5.  Na caixa de diálogo propriedades, clique em **OK.**

Para permitir acesso anônimo não sessecreto a um serviço Web XML, use as seguintes etapas:

1.  Clique com o botão direito **do Meu Computador** ícone na área de trabalho e clique em **Gerenciar**.

2.  Em **Serviços e Aplicativos e** Serviço de Informações da **Internet**, localize o ícone correspondente ao diretório raiz virtual do serviço Web XML. Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.

3.  Na guia **Segurança de** Diretório da caixa de diálogo propriedades, localize **Autenticação** e controle de acesso e clique no **botão Editar** correspondente. Marque a **caixa de seleção Habilitar acesso** anônimo. Clique em **OK**.

4.  Na guia **Segurança de** Diretório da caixa de diálogo propriedades, **localize Comunicações seguras** e clique no **botão Editar** correspondente. Desmarque a caixa de seleção Exigir canal seguro **(SSL).** Clique em **OK**.

5.  Na caixa de diálogo propriedades, clique em **OK.**

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="additional-security-considerations"></a>Considerações adicionais sobre segurança

Ao exigir um canal seguro, você ajuda a proteger a confidencialidade dos dados trocados criptografando as comunicações entre o cliente e seu serviço Web XML. Se você permitir a autenticação usando senhas de texto não limpo, deverá exigir um canal seguro para evitar expor senhas na rede.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo XML](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acessando serviços Web XML no modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Considerações sobre segurança do serviço SOAP COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Criando serviços Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 



