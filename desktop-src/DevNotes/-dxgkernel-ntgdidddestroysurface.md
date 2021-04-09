---
description: Destrói um objeto de superfície do Microsoft DirectDraw previamente alocado no modo kernel.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: Função NtGdiDdDestroySurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 54799aa90007370439b2be8c8cf8c1f584360a5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010187"
---
# <a name="ntgdidddestroysurface-function"></a>Função NtGdiDdDestroySurface

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Destrói um objeto de superfície do Microsoft DirectDraw previamente alocado no modo kernel.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador para objeto de superfície de modo kernel alocado anteriormente.

</dd> <dt>

*bRealDestroy* \[ no\]
</dt> <dd>

Especifica como destruir a superfície. Pode ser um dos valores a seguir.

<dt>



 TRUE


</dt> <dd>

Destrua a superfície e libere memória de vídeo.

</dd> <dt>



 FOR


</dt> <dd>

Libere a memória de vídeo, mas deixe a superfície em um estado não inicializado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdDestroySurface** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_Driver DDHAL \_ manipulado**</dt> </dl>    | O driver executou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, o DirectDraw ou Direct3D continuará com a função. Caso contrário, o DirectDraw ou o Direct3D retorna o código de erro fornecido pelo driver e anula a função.<br/>                                                                                 |
| <dl> <dt>**Driver DDHAL não \_ \_ manipulado**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se for necessário que o driver implementou um retorno de chamada específico, o DirectDraw ou o Direct3D relatará uma condição de erro. Caso contrário, o DirectDraw ou o Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido pela execução da implementação do DirectDraw ou do Direct3D independente de dispositivo.<br/> |



 

## <a name="remarks"></a>Comentários

É recomendável que os aplicativos usem as APIs do DirectDraw e do Direct3D para criar e destruir superfícies em vez dessa função.

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

 

 




