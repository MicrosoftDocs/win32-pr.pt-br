---
description: Retorna o identificador da API do Microsoft DirectX do modo kernel a ser usado em chamadas subsequentes para os pontos de entrada do modo kernel que controlam o mecanismo da API do DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Função NtGdiDdGetDxHandle (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: f1b304216c518765be73d9f3a3e63d39ec4b37fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752930"
---
# <a name="ntgdiddgetdxhandle-function"></a>Função NtGdiDdGetDxHandle

\[Essa função está sujeita a alterações em cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam os aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação direta com os drivers de vídeo.\]

Retorna o identificador da API do Microsoft DirectX do modo kernel a ser usado em chamadas subsequentes para os pontos de entrada do modo kernel que controlam o mecanismo da API do DirectX.

## <a name="syntax"></a>Sintaxe


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hDirectDraw* \[ no\]
</dt> <dd>

Identificador para o objeto do DirectDraw que possui a superfície. Esse parâmetro é opcional e pode ser definido como **nulo**.

</dd> <dt>

*hSurface* \[ no\]
</dt> <dd>

Identificador para superfície para o qual retornar um identificador de API DirectX do modo kernel. Esse parâmetro é opcional e pode ser definido como **nulo**.

</dd> <dt>

*bRelease* \[ no\]
</dt> <dd>

Defina como **true** se a interface do modo kernel da API do DirectX for lançada. Caso contrário, **false**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um identificador de API do DirectX usado em pontos de entrada do kernel com orientação de API do DirectX subsequentes.

## <a name="remarks"></a>Comentários

Se *hDirectDraw* e *hSurface* forem especificados, *hSurface* será ignorado.

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

 

 




