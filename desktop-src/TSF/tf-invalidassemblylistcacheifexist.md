---
title: TF_InvalidAssemblyListCacheIfExist função
description: A função TF \_ InvalidAssemblyListCacheIfExist invalida o cache de descrição do processador de entrada de texto.
ms.assetid: a0f61b25-598c-417c-8679-7523c041f9ef
keywords:
- TF_InvalidAssemblyListCacheIfExist função Estrutura de Serviços de Texto
topic_type:
- apiref
api_name:
- TF_InvalidAssemblyListCacheIfExist
api_location:
- msctf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce85bab9528ccf0fd91988cc52a1d187ac428c856535ae595d65962b32fcfe9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118874543"
---
# <a name="tf_invalidassemblylistcacheifexist-function"></a>Função TF \_ InvalidAssemblyListCacheIfExist

A **função TF \_ InvalidAssemblyListCacheIfExist** invalida o cache de descrição do processador de entrada de texto. Não é necessário chamar essa função se o programa de instalação do processador de entrada exigir que você reinicie ou faça logoff. O cache é válido até que o usuário seja desligado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TF_InvalidAssemblyListCacheIfExist(void);
```



## <a name="parameters"></a>Parâmetros

Essa função não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Essa função pode retornar um desses valores.



| Código de retorno                                                                            | Descrição                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | A função foi bem-sucedida.<br/>   |
| <dl> <dt>**E \_ FAIL**</dt> </dl> | Ocorreu um erro não especificado.<br/> |



 

## <a name="examples"></a>Exemplos

Não há nenhuma biblioteca de importação disponível que defina essa função, portanto, é necessário obter um ponteiro para essa função usando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). O exemplo a seguir demonstra como obter um ponteiro para essa função.

> [!Note]  
> Usar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode comprometer a segurança do seu aplicativo carregando a DLL incorreta. Consulte [Ordem de Pesquisa da Biblioteca de Vínculo](/windows/desktop/Dlls/dynamic-link-library-search-order) Dinâmico para obter informações sobre como carregar DLLs corretamente com versões diferentes do Microsoft Windows.

 


```C++
typedef HRESULT (WINAPI *pTF_InvalidAssemblyListCacheIfExist )(void);

HMODULE hMSCTF = LoadLibrary(TEXT("msctf.dll"));

if(hMSCTF == NULL)
{
    //Error loading module -- fail as securely as possible 
}

else
{
    pTF_InvalidAssemblyListCacheIfExist pfnInvalidAssemblyListCacheIfExist;
    
    pfnInvalidAssemblyListCacheIfExist = (pTF_InvalidAssemblyListCacheIfExist )GetProcAddress(hMSCTF, "TF_InvalidAssemblyListCacheIfExist");

    if(pfnInvalidAssemblyListCacheIfExist)
    {
        (*pfnInvalidAssemblyListCacheIfExist)();
       
    }

    FreeLibrary(hMSCTF);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                      |
| DLL<br/>                      | <dl> <dt>Msctf.dll</dt> </dl> |



 

