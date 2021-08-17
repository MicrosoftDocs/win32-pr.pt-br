---
description: Define tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeração D3DDEVTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d311706d328a5d05668a4d1dcddb032f17fba0c69e48286f899875a8da6a650e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117732986"
---
# <a name="d3ddevtype-enumeration"></a>Enumeração D3DDEVTYPE

Define tipos de dispositivo.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE \_ HAL**
</dt> <dd>

Rasterização de hardware. O sombreamento é feito com software, hardware ou transformação e iluminação misturadas.

</dd> <dt>

<span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**
</dt> <dd>

Inicialize o Direct3D em um computador que não tenha hardware nem rasterização de referência disponíveis e habilita recursos para a criação de conteúdo 3D. Consulte Observações.

</dd> <dt>

<span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ REF**
</dt> <dd>

Os recursos do Direct3D são implementados no software; no entanto, o rasterizador de referência faz uso de instruções especiais de CPU sempre que possível.

O dispositivo de referência é instalado pelo Windows SDK 8.0 ou posterior e destina-se a auxiliar na depuração apenas para desenvolvimento.

</dd> <dt>

<span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**
</dt> <dd>

Um dispositivo de software plug-able que foi registrado com [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).

</dd> <dt>

<span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ FORCE \_ DWORD**
</dt> <dd>

Força essa enumeração a compilar para 32 bits de tamanho. Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada para um tamanho diferente de 32 bits. Este valor não é usado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todos os métodos da interface [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que levam um tipo de dispositivo **D3DDEVTYPE** falharão se D3DDEVTYPE \_ NULLREF for especificado. Para usar esses métodos, substitua D3DDEVTYPE \_ REF na chamada de método.

Um dispositivo REF D3DDEVTYPE deve ser criado na memória SCRATCH de D3DPOOL, a menos que os buffers de \_ \_ vértice e índice sejam necessários. Para dar suporte a buffers de vértice e índice, crie o dispositivo na memória D3DPOOL \_ SYSTEMMEM.

Se D3dref9.dll estiver instalado, o Direct3D usará o rasterizador de referência para criar um tipo de dispositivo REF D3DDEVTYPE, mesmo se \_ D3DDEVTYPE NULLREF for \_ especificado. Se D3dref9.dll estiver disponível e D3DDEVTYPE NULLREF for especificado, o Direct3D não renderizará nem \_ apresentará a cena.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Enumerações direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**IDirect3D9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[**PARÂMETROS DE CRIAÇÃO DE D3DDEVICE \_ \_**](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
