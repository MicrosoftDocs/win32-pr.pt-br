---
description: O acesso a aplicativos COM+ expostos como XML Web Services é controlado pelo servidor Web do IIS, que processa as solicitações de entrada.
ms.assetid: 440b0636-8afc-4fb3-a179-140958948b94
title: Protegendo serviços Web XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94953ce0769c44ddaeda27cacdac99ab4ff252d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812150"
---
# <a name="securing-xml-web-services"></a>Protegendo serviços Web XML

O acesso a aplicativos COM+ expostos como XML Web Services é controlado pelo servidor Web do IIS, que processa as solicitações de entrada. Você também pode configurar o IIS para exigir que as comunicações com o chamador ocorram em um canal seguro estabelecido usando o protocolo protocolo SSL (SSL).

> [!Note]  
> Um serviço Web XML seguro não dá suporte ao acesso WKO via WSDL. Em vez disso, os clientes que instalaram a versão 1,1 do .NET Framework podem chamá-lo no modo CAO. Se os clientes de terceiros precisarem acessar o serviço Web XML via WSDL, você deverá permitir o acesso anônimo.

 

> [!Note]  
> Para usar o protocolo SSL para estabelecer um canal de comunicação seguro, você deve obter e instalar um certificado SSL.

 

## <a name="component-services-administrative-tool"></a>Ferramenta administrativa serviços de componentes

Para selecionar o mecanismo de autenticação para um serviço Web XML, use as seguintes etapas:

1.  Clique com o botão direito do mouse no ícone de **meu computador** na área de trabalho e clique em **gerenciar**.

2.  Em **serviços e aplicativos** e **serviço de informações da Internet**, localize o ícone correspondente ao diretório raiz virtual do seu serviço Web XML. Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.

3.  Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **autenticação e controle de acesso** e clique no botão **Editar** correspondente.

4.  Na caixa de diálogo **métodos de autenticação** , em **acesso autenticado**, use as caixas de seleção para selecionar os mecanismos de autenticação que deseja permitir. Clique em **OK**.

    > [!Note]  
    > Você pode configurar o IIS para autenticar chamadores usando qualquer uma das seguintes opções na caixa de diálogo **métodos de autenticação** do IIS: **autenticação integrada do Windows**, **autenticação Digest para servidores de domínio do Windows**, **autenticação básica (senha enviada em texto não criptografado)** ou **autenticação do .NET Passport**. Você também pode permitir o acesso anônimo.

     

5.  Na caixa de diálogo Propriedades, clique em **OK**.

Para permitir acesso não seguro e anônimo a um serviço Web XML, use as seguintes etapas:

1.  Clique com o botão direito do mouse no ícone de **meu computador** na área de trabalho e clique em **gerenciar**.

2.  Em **serviços e aplicativos** e **serviço de informações da Internet**, localize o ícone correspondente ao diretório raiz virtual do seu serviço Web XML. Clique com o botão direito do mouse no ícone de diretório e escolha **Propriedades**.

3.  Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **autenticação e controle de acesso** e clique no botão **Editar** correspondente. Marque a caixa de seleção **habilitar acesso anônimo** . Clique em **OK**.

4.  Na guia **segurança de diretório** da caixa de diálogo Propriedades, localize **comunicações seguras** e clique no botão **Editar** correspondente. Desmarque a caixa de seleção **exigir canal seguro (SSL)** . Clique em **OK**.

5.  Na caixa de diálogo Propriedades, clique em **OK**.

## <a name="visual-basic"></a>Visual Basic

Não se aplica.

## <a name="cc"></a>C/C++

Não se aplica.

## <a name="additional-security-considerations"></a>Considerações adicionais sobre segurança

Ao exigir um canal seguro, você ajuda a proteger a confidencialidade dos dados trocados criptografando as comunicações entre o cliente e o serviço Web XML. Se você permitir a autenticação usando senhas de texto não criptografado, precisará de um canal seguro para evitar a exposição de senhas na rede.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Acessando serviços Web XML no modo CAO](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Acessando serviços Web XML no modo WKO](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Considerações de segurança do serviço SOAP COM+](com--soap-service-security-considerations.md)
</dt> <dt>

[Criando Serviços Web XML](creating-xml-web-services.md)
</dt> </dl>

 

 



