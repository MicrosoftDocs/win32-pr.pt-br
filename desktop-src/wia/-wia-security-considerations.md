---
description: Este documento fornece informações sobre considerações de segurança relacionadas à WIA (aquisição de imagens do Windows).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Considerações de segurança: aquisição de imagem do Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807939"
---
# <a name="security-considerations-windows-image-acquisition"></a>Considerações de segurança: aquisição de imagem do Windows

Este documento fornece informações sobre considerações de segurança relacionadas à WIA (aquisição de imagens do Windows). Este documento não fornece tudo o que você precisa saber sobre problemas de segurança. em vez disso, use-o como ponto de partida e referência para essa área de tecnologia.

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

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [Home Page de segurança da biblioteca MSDN](https://msdn.microsoft.com/security/default.aspx)
-   [Recursos de instruções de segurança](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [Recursos de segurança do TechNet](https://technet.microsoft.com/security/default.aspx)
-   [Considerações de segurança para desenvolvedores do Windows XP Embedded](/previous-versions/ms838345(v=msdn.10))
-   [Práticas recomendadas de segurança](../secbp/best-practices-for-the-security-apis.md)

 

 
