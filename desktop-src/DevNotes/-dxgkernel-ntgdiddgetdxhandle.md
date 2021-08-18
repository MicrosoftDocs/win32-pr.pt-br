---
description: Retorna o handle da API do Microsoft DirectX no modo kernel a ser usado em chamadas subsequentes para os pontos de entrada no modo kernel que controlam o mecanismo de API do DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: Função NtGdiDdGetDxHandle (Ntgdi.h)
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
ms.openlocfilehash: 13234c7ebe350f096164f0a5de0bde7a60e819e80899aa87258a76727855b869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331916"
---
# <a name="ntgdiddgetdxhandle-function"></a>Função NtGdiDdGetDxHandle

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Retorna o handle da API do Microsoft DirectX no modo kernel a ser usado em chamadas subsequentes para os pontos de entrada no modo kernel que controlam o mecanismo de API do DirectX.

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

*hDirectDraw* \[ Em\]
</dt> <dd>

Identificador para o objeto DirectDraw que possui a superfície. Esse parâmetro é opcional e pode ser definido como **NULL.**

</dd> <dt>

*hSurface* \[ Em\]
</dt> <dd>

Lidar com a superfície para a qual retornar um handle de API directX no modo kernel. Esse parâmetro é opcional e pode ser definido como **NULL.**

</dd> <dt>

*bRelease* \[ Em\]
</dt> <dd>

Definido como **TRUE se** a interface do modo de kernel da API do DirectX deve ser liberada. Caso contrário, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um alça de API do DirectX usado em pontos de entrada de kernel orientados à API do DirectX subsequentes.

## <a name="remarks"></a>Comentários

Se *hDirectDraw* e *hSurface* são especificados, *hSurface* é ignorado.

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

 

 




