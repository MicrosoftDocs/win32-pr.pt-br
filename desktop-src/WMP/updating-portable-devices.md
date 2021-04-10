---
title: Atualizando dispositivos portáteis
description: Atualizando dispositivos portáteis
ms.assetid: 2827e71b-f5e9-4403-9763-043239c4a216
keywords:
- Armazenamentos online do Windows Media Player, atualizando dispositivos portáteis
- lojas online, atualizando dispositivos portáteis
- Digite 1 lojas online, atualizando dispositivos portáteis
- Lojas online do Windows Media Player, dispositivos portáteis
- lojas online, dispositivos portáteis
- tipos 1 lojas online, dispositivos portáteis
- Atualizando dispositivos portáteis
- dispositivos portáteis, atualizando
- dispositivos portáteis, lojas online do Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b29f5314f4eba1af43b3858304f02f8a7e0107df
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293756"
---
# <a name="updating-portable-devices"></a>Atualizando dispositivos portáteis

O Windows Media Player permite que os usuários sincronizem conteúdo de mídia digital com dispositivos portáteis. Isso pode incluir conteúdo de música comprado ou alugado de uma loja online. Em algumas circunstâncias, os provedores de loja online podem querer escrever código para trabalhar em um dispositivo portátil conectado como parte do gerenciamento de conteúdo fornecido pela loja. Para dar ao plug-in da loja online a oportunidade de trabalhar com um dispositivo conectado, o Windows Media Player chama [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice) e fornece o nome canônico do dispositivo portátil. Se o código do plug-in determinar que algum trabalho deve ser feito com o dispositivo conectado, ele deverá retornar imediatamente S \_ OK da chamada para **UpdateDevice** antes de prosseguir para fazer o trabalho. Se não houver nenhum trabalho a fazer, o plug-in deverá retornar um código de erro.

Quando o plug-in terminar de usar o dispositivo, ele deverá chamar [IWMPContentPartnerCallback:: UpdateDeviceComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-updatedevicecomplete) para notificar o Windows Media Player de que o dispositivo está disponível.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de programação para lojas online do tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




