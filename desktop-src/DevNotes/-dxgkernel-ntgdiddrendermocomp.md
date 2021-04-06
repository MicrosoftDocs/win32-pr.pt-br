---
description: Informa ao driver o que macroblocos renderizar especificando as superfícies que contêm o macroblocos, os deslocamentos em cada superfície em que o macroblocos existe e o tamanho dos dados de macrobloco a serem renderizados.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Função NtGdiDdRenderMoComp (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdRenderMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 6e1dd0942a6996264e02531f7e21b2a99f059143
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826137"
---
# <a name="ntgdiddrendermocomp-function"></a>Função NtGdiDdRenderMoComp

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Informa ao driver o que macroblocos renderizar especificando as superfícies que contêm o macroblocos, os deslocamentos em cada superfície em que o macroblocos existe e o tamanho dos dados de macrobloco a serem renderizados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMoComp* \[ no\]
</dt> <dd>

Identificador para uma [**estrutura \_ \_ local MOTIONCOMP DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contém uma descrição da compensação de movimento que está sendo solicitada.

</dd> <dt>

*puRenderMoCompData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ RENDERMOCOMPDATA do DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) que contém as informações necessárias para renderizar um quadro.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdRenderMoComp** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte o Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
