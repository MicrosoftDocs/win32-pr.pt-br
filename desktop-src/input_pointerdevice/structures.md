---
description: Os tópicos nesta seção fornecem as especificações de referência para as estruturas de pilha de entrada do dispositivo ponteiro.
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: Estruturas (entrada de dispositivo de ponteiro)
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/26/2021
ms.locfileid: "105790654"
---
# <a name="pointer-device-input-stack-structures"></a>Estruturas de pilha de entrada do dispositivo ponteiro

Os tópicos nesta seção fornecem as especificações de referência para as estruturas de [pilha de entrada do dispositivo ponteiro](pointer-device-stack-portal.md) .

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|---|---|
| [**POINTER_DEVICE_CURSOR_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | Contém mapeamentos de ID de cursor para dispositivos de ponteiro.<br/> |
| [**POINTER_DEVICE_INFO**](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | Contém informações sobre um dispositivo de ponteiro. Uma matriz dessas estruturas é retornada da função [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) . Uma única estrutura é retornada de uma chamada para a função [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) . <br/> |
| [**POINTER_DEVICE_PROPERTY**](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | Contém as propriedades do dispositivo (dispositivos de interface humana (HID) itens globais que correspondem aos usos de HID).<br/> |

## <a name="related-topics"></a>Tópicos relacionados

[Referência de pilha de entrada do dispositivo ponteiro](unified-input-stack-reference.md)
