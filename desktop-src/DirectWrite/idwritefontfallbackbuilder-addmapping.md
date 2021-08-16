---
title: Método AddMapping IDWriteFontFallbackBuilder
description: Anexa um único mapeamento à lista. Chame isso uma vez para cada mapeamento adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Gravação direta do método AddMapping
- Método AddMapping Direct Write , interface IDWriteFontFallbackBuilder
- IDWriteFontFallbackBuilder interface Direct Write , método AddMapping
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b6496ac9ef9bdfa574cc2c4710ed4620fd855dbf5eff2b22885b32bf343d141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650436"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Método IDWriteFontFallbackBuilder::AddMapping

Anexa um único mapeamento à lista. Chame isso uma vez para cada mapeamento adicional.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Intervalos* 
</dt> <dd>

Tipo: **[ **DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\***

Intervalos Unicode que se aplicam a esse mapeamento.

</dd> <dt>

*rangesCount* 
</dt> <dd>

Tipo: **UINT32**

Número de intervalos Unicode.

</dd> <dt>

*targetFamilyNames* \[ Em\]
</dt> <dd>

Tipo: **const \* \* WCHAR**

Lista de cadeias de caracteres de nome de família de destino.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Tipo: **UINT32**

Número de nomes de família de destino.

</dd> <dt>

*fontCollection* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Coleção de fontes explícitas opcional para esse mapeamento.

</dd> <dt>

*localeName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Localidade do contexto.

</dd> <dt>

*baseFamilyName* \[ in, opcional\]
</dt> <dd>

Tipo: **const \* WCHAR**

Nome da família base para corresponder, se aplicável.

</dd> <dt>

*scale* 
</dt> <dd>

Tipo: **FLOAT**

Fator de escala pelo o que multiplicar a fonte de destino do resultado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Aplicativos UWP de aplicativos da área \[ de trabalho \| R2\]<br/>                          |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

