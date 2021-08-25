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
ms.openlocfilehash: d5aea99e54a43eb35f76c719da885f8d7ae0352d47ecff62b7df38de30410025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950386"
---
# <a name="convertdevmodetoprintticketthunk2-function"></a>Função ConvertDevModeToPrintTicketThunk2

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. [**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

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

*hProvider* \[ Em\]
</dt> <dd>

Um handle para um provedor de tíquete de impressão aberto. Esse handle é retornado pela [**função BindPTProviderThunk.**](bindptproviderthunk.md)

</dd> <dt>

*pDevmode* \[ Em\]
</dt> <dd>

Um ponteiro para o [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) a ser convertido.

</dd> <dt>

*cbSize* \[ Em\]
</dt> <dd>

O tamanho, em bytes, [**do DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode.*

</dd> <dt>

*escopo* \[ Em\]
</dt> <dd>

Um valor que especifica o escopo de *ppPrintTicket*. Esse valor pode especificar uma única página, um documento inteiro ou todos os documentos no trabalho de impressão. O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope,**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) cast como um **DWORD.**

</dd> <dt>

*ppPrintTicket* \[ out\]
</dt> <dd>

O endereço do buffer que contém um tíquete de impressão que representa [**o DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) passado em *pDevmode.* Essa função chama [**CoTaskMemAlloc para**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) alocar esse buffer. Quando o buffer não for mais necessário, o chamador deverá libera-lo chamando [**CoTaskMemFree.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)

</dd> <dt>

*pcbPrintTicketLength* \[ out\]
</dt> <dd>

O tamanho, em bytes, do tíquete de impressão retornado em *ppPrintTicket*.

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

[**PTConvertDevModeToPrintTicket**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertdevmodetoprintticket)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

