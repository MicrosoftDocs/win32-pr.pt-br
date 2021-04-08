---
description: Reposiciona ou modifica os atributos visuais de uma superfície de sobreposição.
ms.assetid: 6d39166c-0efc-450d-adf4-9f4dfdf7c57f
title: Função NtGdiDdUpdateOverlay (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUpdateOverlay
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bbe610c27d83061bda0996ce9acc082efa95e3a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920166"
---
# <a name="ntgdiddupdateoverlay-function"></a>Função NtGdiDdUpdateOverlay

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Reposiciona ou modifica os atributos visuais de uma superfície de sobreposição.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdUpdateOverlay(
  _In_    HANDLE                hSurfaceDestination,
  _In_    HANDLE                hSurfaceSource,
  _Inout_ PDD_UPDATEOVERLAYDATA puUpdateOverlayData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurfaceDestination* \[ no\]
</dt> <dd>

Identificador para objeto DirectDraw do modo de kernel criado anteriormente.

</dd> <dt>

*hSurfaceSource* \[ no\]
</dt> <dd>

Identificador para uma [**estrutura \_ \_ local de superfície do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) que descreve a superfície de sobreposição.

</dd> <dt>

*puUpdateOverlayData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ UPDATEOVERLAYDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_updateoverlaydata) que contém as informações necessárias para atualizar a sobreposição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdUpdateOverlay** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
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

 

 
