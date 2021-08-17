---
description: Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.
ms.assetid: 4aa7b9de-abf2-4781-942e-0b992a6bffed
title: Função MergeAndValidatePrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeAndValidatePrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 156a242d9aa017cc67106a39db6d86809e0ac6f464566205ead09f69fe1b3b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118471669"
---
# <a name="mergeandvalidateprintticketthunk2-function"></a>Função MergeAndValidatePrintTicketThunk2

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. [**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Mescla dois tíquetes de impressão e retorna um tíquete de impressão válido e viável.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT MergeAndValidatePrintTicketThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pBasePrintTicket,
  _In_      INT         basePrintTicketLength,
  _In_opt_  BYTE        *pDeltaPrintTicket,
  _In_      INT         deltaPrintTicketLength,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppValidatedPrintTicket,
  _Out_     INT         *pValidatedPrintTicketLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ Em\]
</dt> <dd>

Um handle para um provedor de tíquete de impressão aberto. Esse handle é retornado pela [**função BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pBasePrintTicket* \[ Em\]
</dt> <dd>

O buffer que contém os dados de tíquete de impressão base, expressos em XML, conforme descrito no [Esquema de Impressão](./printschema.md).

</dd> <dt>

*basePrintTicketLength* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer referenciado por *pBasePrintTicket*.

</dd> <dt>

*pDeltaPrintTicket* \[ in, opcional\]
</dt> <dd>

O buffer que contém o tíquete de impressão a ser mesclado. Os dados do tíquete de impressão são expressos em XML, conforme descrito no [Esquema de Impressão](./printschema.md). O valor desse parâmetro pode ser **NULL.**

</dd> <dt>

*deltaPrintTicketLength* \[ Em\]
</dt> <dd>

O tamanho, em bytes, do buffer referenciado por *pDeltaPrintTicket*.

</dd> <dt>

*escopo* \[ Em\]
</dt> <dd>

O valor que especifica se o escopo *de pDeltaPrintTicket* e *ppValidatedPrintTicket* é uma única página, um documento inteiro ou todos os documentos no trabalho de impressão. O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) cast como um **DWORD.**

</dd> <dt>

*ppValidatedPrintTicket* \[ out\]
</dt> <dd>

O endereço do buffer que contém o tíquete de impressão mesclado e validado. Essa função chama [**CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alocar esse buffer. Quando o buffer não for mais necessário, o chamador deverá libera-lo chamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*pValidatedPrintTicketLength* \[ out\]
</dt> <dd>

O tamanho, em bytes, do buffer referenciado por *ppValidatedPrintTicket*.

</dd> <dt>

*pbstrErrorMessage* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que especifica o que, se algo, é inválido sobre o tíquete de impressão em *pBasePrintTicket* ou *pDeltaPrintTicket*. Se ambos são válidos, esse valor é **NULL.** Se *pbstrErrorMessage* não for **NULL** quando a função retornar, o chamador deverá liberar a cadeia de [**caracteres com SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará S \_ OK;** caso contrário, retornará um **código de erro HRESULT.** Para obter mais informações sobre códigos de erro COM, consulte [Tratamento de erros](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Esquema de impressão](./printschema.md)
</dt> <dt>

[**PTMergeAndValidatePrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptmergeandvalidateprintticket)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

