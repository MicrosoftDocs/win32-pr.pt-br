---
title: Função SetDefaultLayoutOrTipUserReg
description: Define o layout do teclado especificado ou um serviço de texto como um item de entrada padrão do registro do usuário.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Estrutura de serviços de texto da função SetDefaultLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 340e21d8d7416d72361a0e505029500b9a7dde3e53d3388c9311ae3351345c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118875280"
---
# <a name="setdefaultlayoutortipuserreg-function"></a>Função SetDefaultLayoutOrTipUserReg

Define o layout do teclado especificado ou um serviço de texto como um item de entrada padrão do registro do usuário.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
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

*psz* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que representa a lista de layout do teclado ou a lista de perfis de serviços de texto.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um campo de bits que especifica os seguintes sinalizadores:

> [!Note]  
> Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público. Você deve usar o valor hexadecimal ou \# definir os identificadores. Por exemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, você deve incluir \# definir SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 em seu código.

 



| Valor                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Armazena a configuração no registro, mas dose não atualiza a configuração de teclado de tempo de execução da sessão atual. Se o caminho de registro alternativo for definido em **SetDefaultLayoutOrTipUserReg**, esse sinalizador deverá ser definido.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Aplica a configuração imediatamente no thread atual.<br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado



| Código de retorno                                                                          | Descrição                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | A função foi bem-sucedida.<br/>   |
| <dl> <dt>**FOR**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

O formato da cadeia de caracteres da lista de layouts é:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

O formato de cadeia de caracteres da lista de perfis de serviço de texto é:

<LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Veja a seguir um exemplo de um valor para o parâmetro *psz* :


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a>Exemplos

Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). O exemplo a seguir demonstra como obter um ponteiro para essa função.

> [!Note]  
> O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada. Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

