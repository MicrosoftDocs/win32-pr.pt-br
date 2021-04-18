---
title: Atributos de identificação de usuário
description: A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão do NPS em vários atributos diferentes.
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- Atributos, identificação de usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105779388"
---
# <a name="user-identification-attributes"></a>Atributos de identificação de usuário

> [!Note]  
> O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008. O conteúdo deste tópico aplica-se ao IAS e ao NPS. Em todo o texto, o NPS é usado para fazer referência a todas as versões do serviço, incluindo as versões originalmente chamadas de IAS.

 

A identidade do usuário que solicita autenticação é fornecida para as DLLs de extensão do NPS em vários atributos diferentes.

-   **ratUserName**
-   **ratStrippedUserName**
-   **ratFQUserName**

Cada atributo fornece a identidade do usuário em um formato diferente. Em geral, os desenvolvedores devem usar o **ratStrippedUserName**. Os usos dos atributos **ratUserName** e **ratFQUserName** são mais especializados.

> [!Note]  
> O atributo User-Password, **ratUserPassword**, já foi descriptografado quando é enviado para a DLL de extensão e pode ser usado nesse formulário.

 

## <a name="ratusername"></a>ratUserName

O atributo **ratUserName** contém o nome que foi realmente enviado "pela transmissão". O NPS não, de nenhuma forma, processou ou validou o conteúdo deste atributo. Esse atributo pode não estar disponível porque o usuário pode ter sido identificado por meio de um meio, como a ID do chamador.

Ao usar [**RadiusExtensionProcess/ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), se esse atributo estiver disponível, ele estará disponível somente no ponto de plug-in DLL da extensão de autenticação. O atributo **ratUserName** não está disponível no ponto de plug-in DLL da extensão de autorização porque, em DLLs de extensão de autorização, as funções **RadiusExtensionProcess/ex** veem apenas os atributos de "saída".

Ao usar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), se esse atributo estiver disponível, ele estará disponível no ponto de plug-in DLL de extensão de autenticação e no ponto de plug-in DLL de extensão de autorização.

## <a name="ratstrippedusername"></a>ratStrippedUserName

O **ratStrippedUserName** é a identidade do usuário após "remoção de realm". Para obter mais informações sobre a remoção de realm, consulte o tópico [nomes de territórios](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) em http: \\ \\ technet2.Microsoft.com.

Esse atributo pode estar presente no ponto de plug-in de DLL de extensão de autenticação, no ponto de plug-in de DLL de extensão de autorização ou em ambos. É garantido que esse atributo tenha o formato:

*Nome de usuário do domínio ***\\****

Em que *domínio* é o nome de domínio NetBIOS.

## <a name="ratfqusername"></a>ratFQUserName

O atributo **ratFQUserName** é o nome de usuário "totalmente qualificado".

Esse atributo pode estar presente no ponto de plug-in de DLL de extensão de autenticação, no ponto de plug-in de DLL de extensão de autorização ou em ambos. No entanto, o formato do atributo pode ser diferente entre os dois pontos de plug-in. No ponto de plug-in de DLL da extensão de autenticação, esse atributo sempre estará no formato:

*Nome de usuário do domínio ***\\****

O formato do atributo **ratFQUserName** no ponto de plug-in de dll da extensão de autorização depende se o usuário é um usuário Active Directory.

-   Se o usuário for um usuário local, **ratFQUserName** terá o mesmo formato para o ponto de plug-in DLL da extensão de autenticação:

    *Nome de usuário do domínio ***\\****

    .

-   Se o usuário for um usuário Active Directory, **ratFQUserName** poderá conter o nome do usuário no formato "canônico". O formato canônico é o formato usado pelo Active Directory para identificar o usuário. É o caminho da raiz da árvore de Active Directory e inclui a UO (unidade organizacional) do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando as DLLs de extensão](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[Invocando as DLLs de extensão](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 