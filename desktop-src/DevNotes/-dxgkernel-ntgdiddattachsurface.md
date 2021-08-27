---
description: Anexa duas representações de superfície do modo kernel.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: Função NtGdiDdAttachSurface (Ntgdi.h)
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
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088026"
---
# <a name="ntgdiddattachsurface-function"></a>Função NtGdiDdAttachSurface

\[Essa função está sujeita a alterações com cada revisão do sistema operacional. Em vez disso, use o Microsoft DirectDraw e o Microsoft Direct3DAPIs; essas APIs isolam aplicativos dessas alterações do sistema operacional e ocultam muitas outras dificuldades envolvidas na interação diretamente com drivers de exibição.\]

Anexa duas representações de superfície do modo kernel.

## <a name="syntax"></a>Sintaxe


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSurfaceFrom* \[ Em\]
</dt> <dd>

Identificador para o objeto de superfície do modo kernel que será o ponto de partida do novo anexo.

</dd> <dt>

*hSurfaceTo* \[ Em\]
</dt> <dd>

Identificador para o objeto de superfície do modo kernel que será o ponto de extremidade do novo anexo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**NtGdiDdAttachSurface** retorna um dos seguintes:



| Código de retorno                                                                          | Descrição                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**Verdade**</dt> </dl>  | A chamada de função foi bem-sucedida.<br/> |
| <dl> <dt>**False**</dt> </dl> | Falha na chamada de função.<br/>    |



 

## <a name="remarks"></a>Comentários

Consulte o SDK (Software Development Kit) do DirectDraw e o DDK (Kit de Desenvolvimento de Driver) para ver uma descrição completa dos anexos de superfície.

> [!Note]  
> Assim como com outros anexos de superfície, o anexo resultante é one-way. Depois que essa função for chamada, *hSurfaceTo* não será anexado *a hSurfaceFrom*.

 

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

 

 




