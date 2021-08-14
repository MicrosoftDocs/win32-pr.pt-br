---
description: Define a posição de uma sobreposição.
ms.assetid: dd495118-9ceb-4100-a7ec-794659bb4461
title: Função NtGdiDdSetOverlayPosition (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetOverlayPosition
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f4d6b6c11fb2af1aba4b32bb512a5c881239e16ab407f39bbcb82a90dbee7830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386906"
---
# <a name="ntgdiddsetoverlayposition-function"></a>Função NtGdiDdSetOverlayPosition

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Define a posição de uma sobreposição.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdSetOverlayPosition(
  _In_    HANDLE                     hSurfaceSource,
  _In_    HANDLE                     hSurfaceDestination,
  _Inout_ PDD_SETOVERLAYPOSITIONDATA puSetOverlayPositionData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurfaceSource* \[ no\]
</dt> <dd>

Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície de sobreposição do DirectDraw.

</dd> <dt>

*hSurfaceDestination* \[ no\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ \_ local de superfície DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que representa a superfície que está sendo sobreposta.

</dd> <dt>

*puSetOverlayPositionData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ SETOVERLAYPOSITIONDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_setoverlaypositiondata) que contém as informações necessárias para definir a posição da sobreposição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdSetOverlayPosition** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
