---
description: Faz com que a memória da superfície associada ao destino e as superfícies atuais sejam trocadas.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: Função NtGdiDdFlip (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 18113c841c22b31c9768d42491a63ead8cafee3c3b598bc46f442068592e67b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956485"
---
# <a name="ntgdiddflip-function"></a>Função NtGdiDdFlip

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Faz com que a memória da superfície associada ao destino e as superfícies atuais sejam trocadas.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurfaceCurrent* \[ no\]
</dt> <dd>

Identificador para a [estrutura \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície atual.

</dd> <dt>

*hSurfaceTarget* \[ no\]
</dt> <dd>

Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície de destino; ou seja, a superfície à qual o driver deve ser invertido.

</dd> <dt>

*hSurfaceCurrentLeft* \[ no\]
</dt> <dd>

Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície esquerda atual.

</dd> <dt>

*hSurfaceTargetLeft* \[ no\]
</dt> <dd>

Manipule a estrutura [ \_ \_ local da superfície do DD](https://msdn.microsoft.com/library/ms793861.aspx) que descreve a superfície de destino à esquerda para virar.

</dd> <dt>

*puFlipData* \[ entrada, saída\]
</dt> <dd>

Ponteiro para uma [estrutura \_ FLIPDATA do DD](https://msdn.microsoft.com/library/ms794213.aspx) que contém as informações necessárias para executar a inversão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdFlip** retorna um dos seguintes códigos de retorno de chamada.



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

 

 




