---
title: Função SetDefaultLayoutOrTip
description: Define o layout do teclado ou um serviço de texto especificado como o item de entrada padrão do usuário atual.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Estrutura de serviços de texto da função SetDefaultLayoutOrTip
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085320"
---
# <a name="setdefaultlayoutortip-function"></a>Função SetDefaultLayoutOrTip

Define o layout do teclado ou um serviço de texto especificado como o item de entrada padrão do usuário atual.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psz* \[ no\]
</dt> <dd>

Uma cadeia de caracteres que representa uma lista de layout de teclado ou uma lista de perfis de serviços de texto.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Um campo de bits que especifica os sinalizadores a seguir.

> [!Note]  
> Os identificadores a seguir não estão definidos em um arquivo de cabeçalho público. Você deve usar o valor hexadecimal ou \# definir os identificadores. Por exemplo, para usar SDLOT \_ NOAPPLYTOCURRENTSESSION, você deve incluir \# definir SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 em seu código.

 



| Valor                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <dt>**SDLOT \_ NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt> </dl> | Armazena a configuração no registro, mas dose não atualiza a configuração de teclado de tempo de execução da sessão atual. Se o caminho de registro alternativo for definido em [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), esse sinalizador deverá ser definido.<br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <dt>**SDLOT \_ APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt> </dl>          | Aplica a configuração imediatamente no thread atual.<br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor



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
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
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



 

