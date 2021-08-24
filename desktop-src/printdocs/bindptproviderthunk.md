---
description: Abre uma instância de um provedor de tíquetes de impressão.
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
ms.openlocfilehash: 460728eac742fb96ca122981a5874408e12e6c8eddd36fc901e70874e5e040c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720226"
---
# <a name="bindptproviderthunk-function"></a>Função BindPTProviderThunk

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. [**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Abre uma instância de um provedor de tíquetes de impressão.

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

*pszPrinterName* \[ Em\]
</dt> <dd>

O nome completo de uma fila de impressão.

</dd> <dt>

*maxVersion* \[ Em\]
</dt> <dd>

A versão mais recente do [Esquema de Impressão compatível](./printschema.md) com o chamador.

</dd> <dt>

*prefVersion* \[ Em\]
</dt> <dd>

A versão do [Esquema de Impressão](./printschema.md) solicitada pelo chamador.

</dd> <dt>

*phProvider* \[ out\]
</dt> <dd>

Um ponteiro para um ponteiro para o provedor de tíquete de impressão.

</dd> <dt>

*usedVersion* \[ out\]
</dt> <dd>

A versão do Esquema [de Impressão que](./printschema.md) o provedor de tíquete de impressão usará.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele **retornará S \_ OK;** caso contrário, retornará um **código de erro HRESULT.** Para obter mais informações sobre códigos de erro COM, consulte [Tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

Antes de chamar essa função, o thread de chamada deve inicializar COM chamando [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).

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

[**PTOpenProviderEx**](/windows/desktop/api/prntvpt/nf-prntvpt-ptopenproviderex)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

