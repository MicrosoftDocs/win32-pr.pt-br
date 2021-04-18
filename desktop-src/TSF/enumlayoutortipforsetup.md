---
title: Função EnumLayoutOrTipForSetup
description: Enumera os layouts de teclado instalados e os serviços de texto da interface do usuário da instalação ou do OOBE.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Estrutura de serviços de texto da função EnumLayoutOrTipForSetup
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105767780"
---
# <a name="enumlayoutortipforsetup-function"></a>Função EnumLayoutOrTipForSetup

Enumera os layouts de teclado instalados e os serviços de texto da interface do usuário da instalação ou do OOBE.

## <a name="syntax"></a>Sintaxe


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*LangID* \[ no\]
</dt> <dd>

A ID de idioma do item a ser enumerado.

</dd> <dt>

*pLayoutOrTip* \[ fora\]
</dt> <dd>

Ponteiro para o buffer que recebe a matriz de estruturas LAYOUTORTIP. Isso pode ser **nulo** para obter o número de itens.

</dd> <dt>

*uBufLength* \[ no\]
</dt> <dd>

O comprimento do buffer apontado por *pLayoutOrTip*. Isso será ignorado se *pLayoutOrTip* for **nulo**.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Não usado. Isso deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se *pLayoutOrTip* for **nulo**, o número de itens de teclado que são registrados no sistema; caso contrário, o número de itens de teclado que são copiados em *pLayoutOrTip*.

## <a name="remarks"></a>Comentários

Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada. Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.

 

A definição de LAYOUTORTIP é:

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

