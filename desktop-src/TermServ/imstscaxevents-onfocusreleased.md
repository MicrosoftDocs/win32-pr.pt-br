---
title: Método IMsTscAxEvents OnFocusReleased
description: Chamado quando a combinação de teclas de foco da versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona as teclas CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método OnFocusReleased
- Método OnFocusReleased Serviços de Área de Trabalho Remota, interface IMsTscAxEvents
- Serviços de Área de Trabalho Remota de interface IMsTscAxEvents, método OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 673916c3a538f21ceea5b0b7578bb9e8f225ec2a349e38015eab0b50d73935aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512336"
---
# <a name="imstscaxeventsonfocusreleased-method"></a>Método IMsTscAxEvents:: OnFocusReleased

Chamado quando a combinação de teclas de foco da versão é pressionada. Por exemplo, esse evento é chamado quando o usuário pressiona as teclas CTRL + ALT + seta para a esquerda ou CTRL + ALT + seta para a direita.

esse evento permite que o contêiner de controle de ActiveX assuma o controle do controle de ActiveX. Por exemplo, isso é útil em um cenário em que você não tem um mouse e as combinações de teclas especiais, como ALT + TAB, estão sendo redirecionadas para o servidor. Nesse caso, você não tem uma maneira de retornar o foco do teclado de volta para a área de trabalho local. no entanto, com a combinação ctrl + alt + seta para a esquerda ou ctrl + alt + seta para a direita, o contêiner ActiveX pode escutar esse evento e responder, tirando o foco para fora do controle de ActiveX.

## <a name="syntax"></a>Sintaxe


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iDirection* \[ no\]
</dt> <dd>

O parâmetro de direção de 1 (CTRL + ALT + seta direita) ou 1 (CTRL + ALT + seta para esquerda).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse evento está disponível quando Conexão de Área de Trabalho Remota 6,0 é usado no cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents é definido como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





