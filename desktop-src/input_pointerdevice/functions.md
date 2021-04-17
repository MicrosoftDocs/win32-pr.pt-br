---
description: Os tópicos nesta seção fornecem as especificações de referência para funções de pilha de entrada do dispositivo ponteiro.
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: Funções (pilha de entrada do dispositivo ponteiro)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105790652"
---
# <a name="pointer-device-input-stack-functions"></a>Funções de pilha de entrada do dispositivo ponteiro

Os tópicos nesta seção fornecem as especificações de referência para funções de [pilha de entrada do dispositivo ponteiro](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**CreateSyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | Configura o dispositivo de injeção de ponteiro para o aplicativo de chamada e inicializa o número máximo de ponteiros simultâneos que o aplicativo pode injetar.<br/> |
| [**DestroySyntheticPointerDevice**](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | Destrói o dispositivo de injeção de ponteiro especificado.<br/> |
| [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | Obtém informações sobre o dispositivo ponteiro.<br/> |
| [**GetPointerDeviceCursors**](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | Obtém as IDs de cursor que são mapeadas para os cursores associados a um dispositivo ponteiro.<br/> |
| [**GetPointerDeviceProperties**](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | Obtém as propriedades do dispositivo que não estão incluídas na estrutura de [**\_ \_ informações do dispositivo do ponteiro**](/previous-versions/windows/desktop/api) . <br/> |
| [**GetPointerDeviceRects**](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | Obtém o intervalo x e y do dispositivo ponteiro (em HIMETRIC) e o intervalo x e y (resolução atual) para a exibição à qual o dispositivo ponteiro está mapeado. <br/> |
| [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | Obtém informações sobre os dispositivos ponteiros anexados ao sistema.<br/> |
| [**GetRawPointerDeviceData**](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | Obtém os dados brutos de entrada do dispositivo ponteiro. <br/> |
| [**InjectSyntheticPointerInput**](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | Simula a entrada do ponteiro (caneta ou toque).<br/> |
| [**RegisterPointerDeviceNotifications**](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | Registra uma janela para processar as notificações de dispositivo do ponteiro de [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)e [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) .<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Referência de pilha de entrada do dispositivo ponteiro](unified-input-stack-reference.md)
