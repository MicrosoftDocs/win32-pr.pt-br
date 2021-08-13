---
description: este documento fornece informações sobre considerações de segurança relacionadas a WIA (Windows Image Acquisition).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'considerações de segurança: aquisição de imagem de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb8f78e0f45b5b63d5d8deb8ffdd35bc64ee5566ced65ded30ecc51366c0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439675"
---
# <a name="security-considerations-windows-image-acquisition"></a>considerações de segurança: aquisição de imagem de Windows

este documento fornece informações sobre considerações de segurança relacionadas a WIA (Windows Image Acquisition). Este documento não fornece tudo o que você precisa saber sobre problemas de segurança. em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.

-   [Usar aspas ao contrário dos nomes de caminho](#use-quotation-marks-around-path-names)
-   [Coloque os aplicativos registrados em locais seguros](#place-registered-applications-in-secure-locations)
-   [Não usar diretórios subjacentes ou chaves do registro](#do-not-use-underlying-directories-or-registry-keys)
-   [Tópicos relacionados](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Usar aspas ao contrário dos nomes de caminho

Ao usar [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) para registrar um aplicativo para receber eventos de dispositivo, certifique-se de colocar o caminho e o nome de arquivo do aplicativo entre aspas. Isso evita a possibilidade de o caminho ser interpretado erroneamente e um aplicativo não autorizado ser executado.

## <a name="place-registered-applications-in-secure-locations"></a>Coloque os aplicativos registrados em locais seguros

Quando um aplicativo é registrado para receber um evento de dispositivo, esse aplicativo pode ser executado por qualquer usuário que tenha acesso a esse dispositivo. Por exemplo, se um aplicativo for registrado para um evento de verificação, pressionar o botão "Scan" em um scanner fará com que esse aplicativo seja executado. Se o aplicativo for executado com um privilégio maior do que o usuário, isso causará um possível problema de segurança.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Não usar diretórios subjacentes ou chaves do registro

O WIA usa vários diretórios e chaves de registro internamente para armazenar dados ou informações. Não acesse esses diretórios ou chaves do registro diretamente. Em vez disso, use os métodos de interface expostos para especificar diretórios para imagens adquiridas.

## <a name="related-topics"></a>Tópicos relacionados

-   [Segurança da Microsoft](https://www.microsoft.com/security/)
-   [Biblioteca MSDN Home Page de segurança](https://msdn.microsoft.com/security/default.aspx)
-   [Recursos de instruções de segurança](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Recursos de segurança do TechNet](https://technet.microsoft.com/security/default.aspx)
-   [considerações de segurança para desenvolvedores do Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Práticas recomendadas de segurança](../secbp/best-practices-for-the-security-apis.md)

 

 
