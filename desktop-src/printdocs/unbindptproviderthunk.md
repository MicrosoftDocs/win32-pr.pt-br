---
description: Fecha um identificador para um provedor de tíquete de impressão.
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: Função UnbindPTProviderThunk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: e9091360a34a00b7598e50c1b3226d8cc82c82f124602b0308836c61dc8f27ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117685992"
---
# <a name="unbindptproviderthunk-function"></a>Função UnbindPTProviderThunk

\[Essa função não tem suporte e pode ser desabilitada ou excluída em versões futuras do Windows. O [**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) fornece funcionalidade equivalente e deve ser usado em vez disso.\]

Fecha um identificador para um provedor de tíquete de impressão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hProvider* \[ no\]
</dt> <dd>

Um identificador para um provedor de tíquete de impressão aberto. Esse identificador é retornado pela função [**BindPTProviderThunk**](bindptproviderthunk.md) .

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

[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

