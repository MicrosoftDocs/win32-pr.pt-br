---
description: Usado por um CSP (provedor de serviços de criptografia) para verificar a assinatura de uma DLL.
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: Ponteiro de função CRYPT_VERIFY_IMAGE (Cspdk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813108"
---
# <a name="crypt_verify_image-function-pointer"></a>\_Ponteiro de função de imagem de verificação cript \_

A função de retorno de chamada **FuncVerifyImage** é usada por um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para verificar a assinatura de uma dll.

Todas as DLLs auxiliares nas quais um CSP faz chamadas de função devem ser assinadas da mesma maneira (e com a mesma chave) que a DLL do CSP primário. Para garantir essa assinatura, as DLLs auxiliares devem ser carregadas dinamicamente usando a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Mas, antes que a DLL seja carregada, a assinatura da DLL deve ser verificada. O CSP executa essa verificação chamando a função **FuncVerifyImage** , conforme mostrado no exemplo abaixo.

## <a name="syntax"></a>Sintaxe


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszImage* \[ no\]
</dt> <dd>

O endereço de uma cadeia de caracteres terminada em nulo que contém o caminho e o nome do arquivo da DLL para verificar a assinatura.

</dd> <dt>

*pbSigData* \[ no\]
</dt> <dd>

O endereço de um buffer que contém a assinatura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **true** se a função for bem-sucedida, **false** se falhar.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar a função de retorno de chamada **FuncVerifyImage** para verificar a assinatura de uma DLL antes de ser carregada por um CSP.


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
