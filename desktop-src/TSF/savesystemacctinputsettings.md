---
title: Função SaveSystemAcctInputSettings
description: Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive de contas do sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Estrutura de serviços de texto da função SaveSystemAcctInputSettings
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369272"
---
# <a name="savesystemacctinputsettings-function"></a>Função SaveSystemAcctInputSettings

Aplica o layout de teclado do usuário e a configuração de serviço de texto ao hive de contas do sistema.

## <a name="syntax"></a>Sintaxe


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

A janela pai da caixa de diálogo de aviso. A caixa de diálogo de aviso nem sempre é mostrada e aparece adequadamente. Se esse parâmetro for **nulo**, a caixa de diálogo de aviso não será mostrada.

</dd> <dt>

*hSourceRegKey* \[ no\]
</dt> <dd>

A chave do registro raiz da configuração do usuário a ser copiada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                          | Descrição                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**TRUE**</dt> </dl>  | A função foi bem-sucedida.<br/>   |
| <dl> <dt>**FOR**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="remarks"></a>Comentários

O hive da conta do sistema é o HKEY \_ Users \\ . PADRÃO, HKEY \_ Users \\ s-1-5-19 e hKey \_ Users \\ s-1-5-20.

## <a name="examples"></a>Exemplos

Não há biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). O exemplo a seguir demonstra como obter um ponteiro para essa função.

> [!Note]  
> O uso incorreto de [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) pode comprometer a segurança do seu aplicativo carregando a dll errada. Consulte a [ordem de pesquisa da biblioteca de vínculo dinâmico](/windows/desktop/Dlls/dynamic-link-library-search-order) para obter informações sobre como carregar corretamente DLLs com versões diferentes do Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
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



 

