---
title: Função EnumEnabledLayoutOrTip
description: Enumera todos os layouts de teclado ou serviços de texto habilitados da configuração de usuário especificada.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Estrutura de serviços de texto da função EnumEnabledLayoutOrTip
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789469"
---
# <a name="enumenabledlayoutortip-function"></a>Função EnumEnabledLayoutOrTip

Enumera todos os layouts de teclado ou serviços de texto habilitados da configuração de usuário especificada.

## <a name="syntax"></a>Sintaxe


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszUserReg* \[ em, opcional\]
</dt> <dd>

O caminho do registro do usuário. Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.

</dd> <dt>

*pszSystemReg* \[ em, opcional\]
</dt> <dd>

O caminho do registro do sistema. Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.

</dd> <dt>

*pszSoftwareReg* \[ em, opcional\]
</dt> <dd>

O caminho do registro do software. Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.

</dd> <dt>

*pLayoutOrTipProfile* \[ fora\]
</dt> <dd>

Ponteiro para o buffer que recebe a matriz LAYOUTORTIPPROFILE.

</dd> <dt>

*uBufLength* \[ no\]
</dt> <dd>

O comprimento do buffer apontado por *pLayoutOrTipProfile*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se *pLayoutOrTipProfile* for **nulo**, o número de itens de teclado habilitados na configuração de usuário; caso contrário, o número de itens de teclado que são copiados em *pLayoutOrTipProfile*.

Para idiomas do IME (editor de método de entrada), todos os IMEs são retornados, mesmo quando apenas um IME está habilitado. Por exemplo, se um usuário tiver o novo IME rápido do CHT habilitado, a função **EnumEnabledLayoutOrTip** retornará todos os 5 IMEs do CHT.

## <a name="remarks"></a>Comentários

Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada. Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.

 

A definição de LAYOUTORTIPPROFILE é:

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

