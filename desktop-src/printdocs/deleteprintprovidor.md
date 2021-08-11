---
description: A função DeletePrintProvidor remove um provedor de impressão adicionado pela função AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: Função DeletePrintProvidor (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 97870208508f0a0d23b1f3ee2971a3738b8e22b8d6ef7b4252dffb2a7e77289f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235223"
---
# <a name="deleteprintprovidor-function"></a>Função DeletePrintProvidor

A **função DeletePrintProvidor** remove um provedor de impressão adicionado pela [**função AddPrintProvidor.**](addprintprovidor.md)

## <a name="syntax"></a>Sintaxe


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* \[ Em\]
</dt> <dd>

Reservado; deve ser **NULL.**

</dd> <dt>

*pEnvironment* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o provedor deve ser removido (por exemplo, Windows NT x86, Windows IA64 ou Windows x64). Se esse parâmetro for **NULL,** o provedor será removido do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão). **NULL** é o valor recomendado porque fornece portabilidade máxima.

</dd> <dt>

*pPrintProviderName* \[ Em\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do provedor a ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será um valor não zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração do servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool.h (incluir Windows.h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool.lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **DeletePrintProvidorW** (Unicode) e **DeletePrintProvidorA** (ANSI)<br/>                         |



## <a name="see-also"></a>Veja também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




