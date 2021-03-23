---
title: Tratamento de erros e remoção de dispositivo no DirectML
description: Este tópico discute como depurar DirectML dispositivos-remoção e outras condições de erro.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: b4567558b8b75685db16796e921f3daf35b849a1
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548252"
---
# <a name="handling-errors-and-device-removal-in-directml"></a>Tratamento de erros e remoção de dispositivo no DirectML

## <a name="device-removal"></a>Dispositivo-remoção

Se ocorrer um erro irrecuperável, o dispositivo DirectML poderá inserir um estado de "dispositivo removido". Erros irrecuperáveis que causam a remoção de dispositivo incluem uso de API inválido (para métodos que não retornam um [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)), erro de driver, falha de hardware ou condições de OOM (memória insuficiente).

Quando um dispositivo DirectML é removido, todas as chamadas de método no dispositivo e todos os objetos criados por esse dispositivo tornam-se sem operações. Para métodos que retornam um [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes), um código de erro [**DXGI_ERROR_DEVICE_REMOVED**](/windows/desktop/direct3ddxgi/dxgi-error) é retornado. Você pode usar o [método **IDMLDevice:: GetDeviceRemovedReason**](/windows/desktop/api/directml/nf-directml-idmldevice-getdeviceremovedreason) para verificar se o dispositivo DirectML foi removido e para recuperar um código de erro mais detalhado.

Não é possível recuperar-se da remoção do dispositivo, exceto liberando o dispositivo afetado e todos os seus filhos e recriando o dispositivo DirectML do zero.

O dispositivo-remoção do dispositivo Direct3D 12 subjacente também faz com que o dispositivo DirectML seja removido. No entanto, o inverso não é verdadeiro. Dispositivo DirectML-a remoção pode não fazer necessariamente com que o dispositivo Direct3D 12 subjacente seja removido.

## <a name="debugging-directml-device-removal-and-other-errors"></a>Depuração do dispositivo DirectML-remoção e outros erros

A causa mais comum de erros de DirectML é o uso inválido da API. O uso inválido da API pode resultar em um **E_INVALIDARG** código de erro HRESULT ou pode resultar na remoção do dispositivo.

É altamente recomendável que você habilite a [camada de depuração DirectML](dml-debug-layer.md) durante seu desenvolvimento, para detectar e depurar esses erros. A camada de depuração DirectML executa uma extensa validação dos parâmetros do método e do uso da API e emitirá mensagens de saída de depuração para ajudá-lo a depurar.

## <a name="see-also"></a>Confira também

* [Usando a camada de depuração DirectML](dml-debug-layer.md)
