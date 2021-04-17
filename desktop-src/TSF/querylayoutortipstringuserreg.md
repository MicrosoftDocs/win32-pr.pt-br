---
title: Função QueryLayoutOrTipStringUserReg
description: Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto do caminho do registro especificado.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Estrutura de serviços de texto da função QueryLayoutOrTipStringUserReg
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105779913"
---
# <a name="querylayoutortipstringuserreg-function"></a>Função QueryLayoutOrTipStringUserReg

Consulta a cadeia de caracteres especificada que representa o formato de uma lista de layout de teclado ou de perfil de serviços de texto do caminho do registro especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszUserReg* \[ no\]
</dt> <dd>

O caminho do registro do usuário. Se esse parâmetro for **NULL**, hKey \_ Current \_ User será usado.

</dd> <dt>

*pszSystemReg* \[ no\]
</dt> <dd>

O caminho do registro do sistema. Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ System será usado.

</dd> <dt>

*pszSoftwareReg* \[ no\]
</dt> <dd>

O caminho do registro do software. Se esse parâmetro for **NULL**, hKey \_ local \_ Machine \\ software será usado.

</dd> <dt>

*psz* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que representa uma lista de layout de teclado ou uma lista de perfis de serviços de texto.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Isso deve ser 0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função pode retornar um desses valores.



| Código de retorno                                                                                  | Descrição                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Todos os layouts ou perfis definidos em **psz** são válidos.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Um ou mais dos layouts ou perfis definidos em **psz** são inválidos.<br/> |



 

## <a name="remarks"></a>Comentários

Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).

> [!Note]  
> O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada. Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.

 

O formato da cadeia de caracteres da lista de layouts é:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

O formato de cadeia de caracteres da lista de perfis de serviço de texto é:

<LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Veja a seguir um exemplo de um valor para o parâmetro *psz* :

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

