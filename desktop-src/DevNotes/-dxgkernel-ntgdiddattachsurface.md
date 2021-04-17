---
description: Anexa duas representações de superfície no modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Função NtGdiDdAttachSurface (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: a3d099e7b3a3106e0e1e4285b37d2ea205baf3d5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755816"
---
# <a name="ntgdiddattachsurface-function"></a>Função NtGdiDdAttachSurface

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Anexa duas representações de superfície no modo kernel.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurfaceFrom* \[ no\]
</dt> <dd>

Identificador do objeto de superfície do modo kernel que será o ponto inicial do novo anexo.

</dd> <dt>

*hSurfaceTo* \[ no\]
</dt> <dd>

Identificador do objeto de superfície do modo kernel que será o ponto final do novo anexo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**NtGdiDdAttachSurface** retorna um dos seguintes:



| Código de retorno                                                                          | Descrição                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | A chamada de função foi bem-sucedida.<br/> |
| <dl> <dt>**FOR**</dt> </dl> | Falha na chamada de função.<br/>    |



 

## <a name="remarks"></a>Comentários

Consulte o DirectDraw Software Development Kit (SDK) e o Driver Development Kit (DDK) para obter uma descrição completa dos anexos de superfície.

> [!Note]  
> Assim como ocorre com outros anexos de superfície, o anexo resultante é unidirecional. Depois que essa função for chamada, *hSurfaceTo* não será anexado a *hSurfaceFrom*.

 

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

 

 




