---
description: Abre uma instância de um provedor de tíquete de impressão.
ms.assetid: 815cc360-8dcd-4c58-a64d-5d77436a8623
title: Função BindPTProviderThunk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: bf63fc6faf9d47993fafb97c8d3a1c18d6d6c985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169352"
---
# <a name="bindptproviderthunk-function"></a>Função BindPTProviderThunk

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. O [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Abre uma instância de um provedor de tíquete de impressão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT BindPTProviderThunk(
  _In_  LPTSTR      pszPrinterName,
  _In_  INT         maxVersion,
  _In_  INT         prefVersion,
  _Out_ HPTPROVIDER *phProvider,
  _Out_ INT         *usedVersion
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszPrinterName* \[ no\]
</dt> <dd>

O nome completo de uma fila de impressão.

</dd> <dt>

*MaxVersion* \[ no\]
</dt> <dd>

A versão mais recente do [esquema de impressão](./printschema.md) que o chamador dá suporte.

</dd> <dt>

*prefVersion* \[ no\]
</dt> <dd>

A versão do [esquema de impressão](./printschema.md) solicitado pelo chamador.

</dd> <dt>

*phProvider* \[ fora\]
</dt> <dd>

Um ponteiro para um identificador para o provedor de tíquete de impressão.

</dd> <dt>

*usedVersion* \[ fora\]
</dt> <dd>

A versão do [esquema de impressão](./printschema.md) que o provedor de tíquete de impressão usará.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará **S \_ OK**; caso contrário, ele retornará um código de erro **HRESULT** . Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

Antes de chamar essa função, o thread de chamada deve inicializar COM chamando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

