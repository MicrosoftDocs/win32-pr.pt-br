---
title: Função InstallLayoutOrTipUserReg
description: Habilita os layouts de teclado ou os serviços de texto especificados para o usuário especificado.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Estrutura de serviços de texto da função InstallLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644681"
---
# <a name="installlayoutortipuserreg-function"></a>Função InstallLayoutOrTipUserReg

Habilita os layouts de teclado ou os serviços de texto especificados para o usuário especificado.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
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

Um campo de bits que especifica os sinalizadores a seguir.

> [!Note]  
> Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público. Você deve usar o valor hexadecimal ou \# definir os identificadores. Por exemplo, para usar **a \_ desinstalação do ILOT** , você deve incluir `#define ILOT_UNINSTALL 0x00000001` em seu código.

 



| Valor                                                                                                                                                                                                                                                                      | Significado                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <dt>**ILOT \_ DESINSTALAR**</dt> <dt>0x00000001</dt> </dl>                                           | O mesmo que **ILOT \_ desabilitado**.<br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <dt>**ILOT \_ DEFPROFILE**</dt> <dt>0x00000002</dt> </dl>                                        | Define o layout ou a dica especificado como um item padrão.<br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <dt>**ILOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt> </dl> | A configuração é salva, mas não é aplicada à sessão atual.<br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <dt>**ILOT \_ CLEANINSTALL**</dt> <dt>0x00000040</dt> </dl>                                  | Desabilita todos os layouts de teclado e serviços de texto atuais.<br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <dt>**ILOT \_ 0x00000080 DESABILITAdo**</dt> <dt></dt> </dl>                                              | Desabilita o layout de teclado e o serviço de texto especificados.<br/>        |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                         | Description                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl> | A função foi bem-sucedida.<br/>   |
| <dl> <dt>**FASE**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

O formato da cadeia de caracteres da lista de layouts é:

<LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N>

O formato de cadeia de caracteres da lista de perfis de serviço de texto é:

<LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};

Veja a seguir um exemplo de um valor para o parâmetro *psz* :


```C++
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
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

