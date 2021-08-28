---
description: Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: Função RtlIsValidLocaleName (Ntrtl.h)
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
ms.openlocfilehash: 993d819324987fccdfb66c26343bccfb9a815606655a18ff1a1e43f9a2af0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130276"
---
# <a name="rtlisvalidlocalename-function"></a>Função RtlIsValidLocaleName

Determina se uma localidade especificada pelo nome está instalada ou tem suporte no sistema operacional.

> [!Note]  
> Essa função está disponível para uso somente Windows Vista. Ele pode ser alterado ou não disponível nas versões subsequentes. Os aplicativos devem [**usar IsValidLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LocaleName* \[ Em\]
</dt> <dd>

[Nome da localidade a](locale-names.md) ser validado. Esse parâmetro pode especificar o nome de uma [localidade personalizada.](custom-locales.md)

</dd> <dt>

*Sinalizadores* \[ Em\]
</dt> <dd>

Sinalizadores que indicam se localidades neutras são consideradas válidas. Atualmente, o único sinalizador definido é [LOCALE \_ ALLOW \_ NEUTRAL.](locale-allow-neutral.md) O valor padrão é que eles não são.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará um valor diferente de zero se for bem-sucedido ou 0 caso contrário.

## <a name="remarks"></a>Comentários

Essa função é semelhante a [**IsValidLocaleName.**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) A única diferença é que, se LOCALE ALLOW NEUTRAL estiver \_ \_ definido, **RtlIsValidLocaleName**  retornará TRUE para um nome que corresponda a uma localidade neutra (como "en"), enquanto [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) **retornará TRUE** somente para uma localidade específica (como "en-US"). Localidades neutras são usadas como parte da estratégia de carregamento de recursos no Windows Vista e posterior. Somente uma pequena classe de aplicativos altamente especializados usa **RtlIsValidLocaleName** e definir LOCALE ALLOW NEUTRAL, pois localidades neutras são de \_ \_ uso muito limitado. Nenhuma das funções descritas em Chamar as funções ["Nome da Localidade"](calling-the--locale-name--functions.md) aceita localidades neutras como entradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ntrtl.h</dt> </dl>      |
| Biblioteca<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Suporte a idiomas nacionais](national-language-support.md)
</dt> <dt>

[Funções de suporte a idiomas nacionais](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




