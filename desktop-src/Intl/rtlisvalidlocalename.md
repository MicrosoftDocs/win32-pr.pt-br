---
description: Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Função RtlIsValidLocaleName (Ntrtl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 3433daaf48e81f662945f1d223e9cf7188ddb706
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827056"
---
# <a name="rtlisvalidlocalename-function"></a>Função RtlIsValidLocaleName

Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.

> [!Note]  
> Essa função está disponível para uso somente no Windows Vista. Ele pode ser alterado ou indisponível nas versões subsequentes. Os aplicativos devem usar o [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename).

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Localename* \[ no\]
</dt> <dd>

[Nome da localidade](locale-names.md) para validar. Esse parâmetro pode especificar o nome de uma [localidade personalizada](custom-locales.md).

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Sinalizadores que indicam se as localidades neutras são consideradas válidas. Atualmente, o único sinalizador definido é a [localidade \_ permitir \_ neutro](locale-allow-neutral.md). O valor padrão é que eles não são.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor diferente de zero se for bem-sucedido ou 0 caso contrário.

## <a name="remarks"></a>Comentários

Essa função é semelhante a [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename). A única diferença é que, se \_ a localidade permitir \_ neutro for definida, **RtlIsValidLocaleName** retornará **true** para um nome que corresponda a uma localidade neutra (como "en"), enquanto [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) retorna **true** somente para uma localidade específica (como "en-US"). As localidades neutras são usadas como parte da estratégia de carregamento de recursos no Windows Vista e versões posteriores. Apenas uma pequena classe de aplicativos altamente especializados usa **RtlIsValidLocaleName** e define a \_ localidade \_ como neutra, pois as localidades neutras são de uso muito limitado. Nenhuma das funções descritas na [chamada das funções "nome de localidade"](calling-the--locale-name--functions.md) aceita localidades neutras como entradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Ntrtl. h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte ao idioma nacional](national-language-support.md)
</dt> <dt>

[Funções de suporte ao idioma nacional](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




