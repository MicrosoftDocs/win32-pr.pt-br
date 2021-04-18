---
description: Converte uma estrutura DEVMODE em um tíquete de impressão.
ms.assetid: c03371f8-a978-4fb7-82cc-f76a65f3904c
title: Função ConvertDevModeToPrintTicketThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertDevModeToPrintTicketThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: f13d597a11a4d6cfd1ad6f5d70b3a386560f5106
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785321"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>Função ConvertDevModeToPrintTicketThunk2

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. O [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Converte uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) em um tíquete de impressão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertDevModeToPrintTicketThunk2(
  _In_  HPTPROVIDER hProvider,
  _In_  BYTE        *pDevmode,
  _In_  ULONG       cbSize,
  _In_  DWORD       scope,
  _Out_ BYTE        **ppPrintTicket,
  _Out_ INT         *pcbPrintTicketLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ no\]
</dt> <dd>

Um identificador para um provedor de tíquete de impressão aberto. Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .

</dd> <dt>

*pDevmode* \[ no\]
</dt> <dd>

Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser convertido.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

O tamanho, em bytes, do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode*.

</dd> <dt>

*escopo* \[ no\]
</dt> <dd>

Um valor que especifica o escopo de *ppPrintTicket*. Esse valor pode especificar uma única página, um documento inteiro ou todos os documentos no trabalho de impressão. O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , Cast como um **DWORD**.

</dd> <dt>

*ppPrintTicket* \[ fora\]
</dt> <dd>

O endereço do buffer que contém um tíquete de impressão que representa o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode*. Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer. Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbPrintTicketLength* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do tíquete de impressão retornado em *ppPrintTicket*.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** . Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Prntvpt.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Imprimir esquema](./printschema.md)
</dt> <dt>

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

