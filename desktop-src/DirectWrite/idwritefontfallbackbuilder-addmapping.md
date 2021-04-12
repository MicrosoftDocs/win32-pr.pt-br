---
title: Método AddMapping IDWriteFontFallbackBuilder
description: Anexa um único mapeamento à lista. Chame isso uma vez para cada mapeamento adicional.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Método AddMapping Direct Write
- Método AddMapping Direct Write, interface IDWriteFontFallbackBuilder
- Interface IDWriteFontFallbackBuilder Direct Write, Método AddMapping
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
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369747"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a>Método IDWriteFontFallbackBuilder:: AddMapping

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

*varia* 
</dt> <dd>

Tipo: **\* [**\_ \_ intervalo Unicode DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)* _

Intervalos Unicode que se aplicam a esse mapeamento.

</dd> <dt>

_rangesCount * 
</dt> <dd>

Tipo: **UINT32**

Número de intervalos Unicode.

</dd> <dt>

*targetFamilyNames* \[ no\]
</dt> <dd>

Tipo: **const WCHAR \* \***

Lista de cadeias de caracteres de nome de família de destino.

</dd> <dt>

*targetFamilyNamesCount* 
</dt> <dd>

Tipo: **UINT32**

Número de nomes de família de destino.

</dd> <dt>

*fonte de fontes* \[ em, opcional\]
</dt> <dd>

Tipo: **[ **IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**

Coleção de fontes explícita opcional para este mapeamento.

</dd> <dt>

*localename* \[ em, opcional\]
</dt> <dd>

Tipo: **const WCHAR \** _

Localidade do contexto.

</dd> <dt>

_baseFamilyName * \[ in, opcional\]
</dt> <dd>

Tipo: **const WCHAR \** _

Nome da família base com a qual corresponder, se aplicável.

</dd> <dt>

_scale * 
</dt> <dd>

Tipo: **float**

Fator de escala para multiplicar a fonte de destino do resultado por.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]<br/>                          |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/> |
| Biblioteca<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md)
</dt> </dl>

 

