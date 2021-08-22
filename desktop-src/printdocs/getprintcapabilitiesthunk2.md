---
description: Recupera os recursos de impressoras formatados em conformidade com o esquema de impressão XML.
ms.assetid: 15219c19-b64c-4c51-9357-15a797557693
title: Função GetPrintCapabilitiesThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintCapabilitiesThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: 55127d15eae41380fd5376ca54589488e255a740a7881042f54bc203873701f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971385"
---
# <a name="getprintcapabilitiesthunk2-function"></a>Função GetPrintCapabilitiesThunk2

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. O [**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Recupera os recursos da impressora formatados em conformidade com o [esquema de impressão](./printschema.md)XML.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPrintCapabilitiesThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      INT         cbPrintTicket,
  _Out_     BYTE        **ppbPrintCapabilities,
  _Out_     INT         *pcbPrintCapabilitiesLength,
  _Out_opt_ BSTR        *pbstrErrorMessage
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ no\]
</dt> <dd>

Um identificador para um provedor de tíquete de impressão aberto. Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pPrintTicket* \[ no\]
</dt> <dd>

O buffer que contém os dados de tíquete de impressão, expressos em XML, conforme descrito no [esquema de impressão](./printschema.md).

</dd> <dt>

*cbPrintTicket* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer referenciado por *pPrintTicket*.

</dd> <dt>

*ppbPrintCapabilities* \[ fora\]
</dt> <dd>

O endereço do buffer que é alocado por essa função e contém as informações válidas de recursos de impressão, codificados como XML. Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer. Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintCapabilitiesLength* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do buffer referenciado por *ppbPrintCapabilities*.

</dd> <dt>

*pbstrErrorMessage* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que especifica o que, se for algo, é inválido sobre *pPrintTicket*. Se for válido, esse valor será **NULL**. Se *pbstrErrorMessage* não for **nulo** quando a função retornar, o chamador deverá liberar a cadeia de caracteres com [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** . Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PTGetPrintCapabilities**](/windows/desktop/api/prntvpt/nf-prntvpt-ptgetprintcapabilities)
</dt> <dt>

[Imprimir esquema](./printschema.md)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

