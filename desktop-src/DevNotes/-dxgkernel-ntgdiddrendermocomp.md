---
description: Informa ao driver quais macroblocks renderizar especificando as superfícies que contêm os macroblocks, os deslocamentos em cada superfície em que os macroblocks existem e o tamanho dos dados de macroblock a serem renderizados.
ms.assetid: c49d9dfa-a3db-4572-a474-72c7d4e80940
title: Função NtGdiDdRenderMoComp (Ntgdi.h)
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
ms.openlocfilehash: d057ba1c7b533d75ce10754670b911ddc01a689acee29d79614a3ce2f273d278
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827967"
---
# <a name="ntgdiddrendermocomp-function"></a>Função NtGdiDdRenderMoComp

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Informa ao driver quais macroblocks renderizar especificando as superfícies que contêm os macroblocks, os deslocamentos em cada superfície em que os macroblocks existem e o tamanho dos dados de macroblock a serem renderizados.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdRenderMoComp(
  _In_    HANDLE               hMoComp,
  _Inout_ PDD_RENDERMOCOMPDATA puRenderMoCompData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMoComp* \[ Em\]
</dt> <dd>

Lidar com uma [**estrutura DD \_ MOTIONCOMP \_ LOCAL**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) que contém uma descrição da compensação de movimento que está sendo solicitada.

</dd> <dt>

*puRenderMoCompData* \[ in, out\]
</dt> <dd>

Ponteiro para uma [**estrutura \_ RENDERMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_rendermocompdata) que contém as informações necessárias para renderizar um quadro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdRenderMoComp** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ MANIPULADO**</dt> </dl>    | O driver realizou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, DirectDraw ou Direct3D prosseguirá com a função . Caso contrário, DirectDraw ou Direct3D retornará o código de erro fornecido pelo driver e anulará a função.<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ DRIVER \_ NOTHANDLED**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se o driver precisar ter implementado um retorno de chamada específico, DirectDraw ou Direct3D relata uma condição de erro. Caso contrário, DirectDraw ou Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido executando a implementação independente de dispositivo DirectDraw ou Direct3D.<br/> |



 

## <a name="remarks"></a>Comentários

Para obter mais informações, consulte O DDK (Kit de Desenvolvimento de Driver de Aceleração de Vídeo) do Microsoft DirectX.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Ntgdi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao cliente de nível baixo de gráficos](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
