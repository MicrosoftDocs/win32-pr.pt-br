---
title: Atributos de identificação do usuário
description: A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão nps em vários atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, Identificação do Usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff099b46844f2259ad127346bb1ee2bfafccf4b116f3dba86dff3e175d11c28c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128756"
---
# <a name="user-identification-attributes"></a>Atributos de identificação do usuário

> [!Note]  
> O IAS (Serviço de Autenticação da Internet) foi renomeado como NPS (Servidor de Políticas de Rede) a partir do Windows Server 2008. O conteúdo deste tópico se aplica a IAS e NPS. Em todo o texto, o NPS é usado para se referir a todas as versões do serviço, incluindo as versões originalmente conhecidas como IAS.

 

A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão nps em vários atributos diferentes.

-   **lusUserName**
-   **stripStrippedUserName**
-   **fmFQUserName**

Cada atributo fornece a identidade do usuário em um formato diferente. Em geral, os desenvolvedores devem **usar o stripStrippedUserName**. Os usos dos **atributos ltdUserName** e **fmFQUserName** são mais especializados.

> [!Note]  
> O User-Password, o **atributo ,lusUserPassword**, já foi descriptografado quando é enviado para a DLL de extensão e é utilizável nesse formato.

 

## <a name="ratusername"></a>lusUserName

O **atributolususerName** contém o nome que foi realmente enviado "pela transmissão". O NPS não processou ou validou o conteúdo desse atributo. Esse atributo pode não estar disponível porque o usuário pode ter sido identificado por meio de um meio, como a ID do chamador.

Ao usar [**RadiusExtensionProcess/Ex,**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)se esse atributo estiver disponível, ele estará disponível somente no ponto de plug-in DLL da Extensão de Autenticação. O **atributo ltdUserName** não está disponível no ponto de plug-in DLL da Extensão de Autorização porque, em DLLs de Extensão de Autorização, as funções **RadiusExtensionProcess/Ex** veem apenas os atributos de "saída".

Ao usar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), se esse atributo estiver disponível, ele estará disponível no ponto de plug-in DLL da Extensão de Autenticação e no ponto de plug-in DLL da Extensão de Autorização.

## <a name="ratstrippedusername"></a>stripStrippedUserName

O **the stripStrippedUserName** é a identidade do usuário após a "remoção de realm". Para obter mais informações sobre a remoção de realm, consulte o [tópico Nomes de realm](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) em http: \\ \\ technet2.microsoft.com.

Esse atributo pode estar presente no ponto de plug-in da DLL da Extensão de Autenticação, no ponto de plug-in DLL da Extensão de Autorização ou em ambos. Esse atributo tem a garantia de ter o formato:

*Domain* **\\** _UserName_

Em *que Domain* é o nome de domínio NetBIOS.

## <a name="ratfqusername"></a>fmFQUserName

O **atributo graveFQUserName** é o nome de usuário "totalmente qualificado".

Esse atributo pode estar presente no ponto de plug-in da DLL da Extensão de Autenticação, no ponto de plug-in DLL da Extensão de Autorização ou em ambos. No entanto, o formato do atributo pode ser diferente entre os dois pontos de plug-in. No ponto de plug-in da DLL da Extensão de Autenticação, esse atributo sempre estará no formato:

*Domain* **\\** _UserName_

O formato do **atributo chromeFQUserName no** ponto de plug-in da DLL da Extensão de Autorização depende se o usuário é um usuário do Active Directory.

-   Se o usuário for um usuário **local, o fmFQUserName** terá o mesmo formato do ponto de plug-in da DLL da Extensão de Autenticação:

    *Domain* **\\** _UserName_

    .

-   Se o usuário for um usuário do Active Directory, **o fmFQUserName** poderá conter o nome do usuário no formato "canônico". Formato canônico é o formato usado pelo Active Directory para identificar o usuário. É o caminho da raiz da árvore do Active Directory e inclui a UO (Unidade Organizacional) do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Invocando as DLLs de extensão](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 