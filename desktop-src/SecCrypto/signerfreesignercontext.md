---
description: Libera uma estrutura de \_ contexto de signatário alocada por uma chamada anterior à função SignerSignEx.
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: Função SignerFreeSignerContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755035"
---
# <a name="signerfreesignercontext-function"></a>Função SignerFreeSignerContext

A função **SignerFreeSignerContext** libera uma estrutura [**de \_ contexto de signatário**](signer-context.md) alocada por uma chamada anterior à função [**SignerSignEx**](signersignex.md) .

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário e usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSignerContext* \[ no\]
</dt> <dd>

Um ponteiro para a estrutura de [**\_ contexto do assinante**](signer-context.md) como gratuito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, a função retornará S \_ OK.

Se a função falhar, ela retornará um valor **HRESULT** que indica o erro. Para obter uma lista de códigos de erro comuns, consulte [valores comuns de HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**contexto do ASSINAnte \_**](signer-context.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
