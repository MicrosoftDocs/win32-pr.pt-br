---
title: Método GetClassInstance ID3DX11EffectClassInstanceVariable (D3dx11effect.h)
description: Obtém uma instância de classe.
ms.assetid: dec00a6b-0587-40cf-abae-dd110a639fe0
keywords:
- Método GetClassInstance Direct3D 11
- Método GetClassInstance Direct3D 11 , interface ID3DX11EffectClassInstanceVariable
- ID3DX11EffectClassInstanceVariable interface Direct3D 11 , método GetClassInstance
topic_type:
- apiref
api_name:
- ID3DX11EffectClassInstanceVariable.GetClassInstance
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0f188c1ef72b688b4c1f227bac91139b5c6cfcb2749a5f2c1fa41dd61a179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046444"
---
# <a name="id3dx11effectclassinstancevariablegetclassinstance-method"></a>Método ID3DX11EffectClassInstanceVariable::GetClassInstance

Obtém uma instância de classe.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetClassInstance(
   ID3D11ClassInstance **ppClassInstance
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppClassInstance* 
</dt> <dd>

Tipo: **[ **ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)\*\***

Ponteiro para um [**ponteiro ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) que será definido como instância de classe.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna um dos códigos de [retorno do Direct3D 11 a seguir.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

> [!Note]  
> O SDK do DirectX não fornece binários compilados para efeitos. Você deve usar a origem efeitos 11 para criar seu aplicativo do tipo efeitos. Para obter mais informações sobre como usar a origem dos Efeitos 11, consulte [Diferenças entre efeitos 10 e efeitos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (uma biblioteca effects 11 está disponível online como fonte compartilhada.)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ID3DX11EffectClassInstanceVariable](id3dx11effectclassinstancevariable.md)
</dt> </dl>

 

 





