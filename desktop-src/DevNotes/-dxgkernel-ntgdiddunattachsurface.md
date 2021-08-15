---
description: Remove um anexo, criado com NtGdiDdAttachSurface, entre dois objetos de superfície de modo kernel.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: Função NtGdiDdUnattachSurface (Ntgdi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7bc5abd09c9a7372bb693a3220d2f059e393ed2df17af87c1187b9c927fdb627
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386866"
---
# <a name="ntgdiddunattachsurface-function"></a>Função NtGdiDdUnattachSurface

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Remove um anexo, criado com [**NtGdiDdAttachSurface,**](-dxgkernel-ntgdiddattachsurface.md)entre dois objetos de superfície de modo kernel.

## <a name="syntax"></a>Sintaxe


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurface* \[ Em\]
</dt> <dd>

O objeto de superfície do modo kernel que foi passado como o parâmetro hSurfaceFrom para [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).

</dd> <dt>

*hSurfaceAttached* \[ Em\]
</dt> <dd>

O objeto de superfície do modo kernel que foi passado como o parâmetro hSurfaceTo para [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdUnattachSurface** retorna um dos seguintes códigos de retorno de chamada.



| Código de retorno                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DRIVER DDHAL \_ \_ MANIPULADO**</dt> </dl>    | O driver realizou a operação e retornou um código de retorno válido para essa operação. Se esse código for DD \_ OK, DirectDraw ou Direct3D prosseguirá com a função . Caso contrário, DirectDraw ou Direct3D retornará o código de erro fornecido pelo driver e anulará a função.<br/>                                                                                 |
| <dl> <dt>**DDHAL \_ DRIVER \_ NOTHANDLED**</dt> </dl> | O driver não tem nenhum comentário sobre a operação solicitada. Se o driver precisar ter implementado um retorno de chamada específico, DirectDraw ou Direct3D relata uma condição de erro. Caso contrário, DirectDraw ou Direct3D tratará a operação como se o retorno de chamada do driver não tivesse sido definido executando a implementação independente de dispositivo DirectDraw ou Direct3D.<br/> |



 

## <a name="remarks"></a>Comentários

É recomendável que os aplicativos usem a API do DirectDraw, que lida com anexos de superfície de maneira de nível superior.

Não é necessário chamar essa função porque o kernel destruirá automaticamente todos os anexos quando [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) for chamado.

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

 

 




