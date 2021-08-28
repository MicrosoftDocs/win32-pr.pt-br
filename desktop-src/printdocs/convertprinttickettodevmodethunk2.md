---
description: Converte um tíquete de impressão em uma estrutura DEVMODE.
ms.assetid: 3b0a6afd-fa9d-434e-a95f-b051296d4567
title: Função ConvertPrintTicketToDevModeThunk2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertPrintTicketToDevModeThunk2
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: e6325ca61d18d571a3a3b346b18f6191b53e43d2ce96799c34a643477123f20c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112676"
---
# <a name="convertprinttickettodevmodethunk2-function"></a>Função ConvertPrintTicketToDevModeThunk2

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. O [**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Converte um tíquete de impressão em uma estrutura [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConvertPrintTicketToDevModeThunk2(
  _In_      HPTPROVIDER hProvider,
  _In_      BYTE        *pPrintTicket,
  _In_      ULONG       cbSize,
  _In_      INT         baseType,
  _In_      DWORD       scope,
  _Out_     BYTE        **ppDevmode,
  _Out_     ULONG       *pcbDevModeLength,
  _Out_opt_ BSTR        *errMsg
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

O buffer que contém o tíquete de impressão a ser convertido.

</dd> <dt>

*cbSize* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer passado em *pPrintTicket*.

</dd> <dt>

*BaseType* \[ no\]
</dt> <dd>

Um valor que indica se [**o DEVMODE padrão do usuário ou o**](/windows/win32/api/wingdi/ns-wingdi-devmodea) **DEVMODE** padrão da fila de impressão é usado para fornecer valores para o **DEVMODE** de saída quando *pPrintTicket* não especifica todas as configurações possíveis para um **DEVMODE**. O valor desse parâmetro deve ser um membro da enumeração [**EDefaultDevmodeType**](/windows/win32/api/prntvpt/ne-prntvpt-edefaultdevmodetype) , Cast como um **int**.

</dd> <dt>

*escopo* \[ no\]
</dt> <dd>

Um valor que especifica o escopo de *pPrintTicket*. Esse valor pode especificar uma única página, um documento inteiro ou todos os documentos no trabalho de impressão. O valor desse parâmetro deve ser um membro da enumeração [**EPrintTicketScope**](/windows/desktop/api/prntvpt/ne-prntvpt-eprintticketscope) , Cast como um **DWORD**.

</dd> <dt>

*ppDevmode* \[ fora\]
</dt> <dd>

O endereço do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)recém-criado. Essa função chama [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) para alocar esse buffer. Quando o buffer não for mais necessário, o chamador deverá liberá-lo chamando [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree).

</dd> <dt>

*pcbDevModeLength* \[ fora\]
</dt> <dd>

O tamanho, em bytes, do [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) retornado em *ppDevmode*.

</dd> <dt>

*errMsg* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que especifica o que, se for algo, é inválido sobre o tíquete de impressão no *pPrintTicket*. Se for válido, isso será **nulo**. Se *errMsg* não for **nulo** quando a função retornar, o chamador deverá liberar a cadeia de caracteres com [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

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

[Imprimir esquema](./printschema.md)
</dt> <dt>

[**PTConvertPrintTicketToDevMode**](/windows/desktop/api/prntvpt/nf-prntvpt-ptconvertprinttickettodevmode)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

