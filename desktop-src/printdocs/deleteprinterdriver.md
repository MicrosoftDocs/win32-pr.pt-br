---
description: A função DeletePrinterDriver remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Função DeletePrinterDriver (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748362"
---
# <a name="deleteprinterdriver-function"></a>Função DeletePrinterDriver

A função **DeletePrinterDriver** remove o nome de driver de impressora especificado da lista de nomes de drivers com suporte em um servidor.

Para excluir os arquivos associados ao driver, além de remover o nome de driver de impressora especificado da lista de nomes de drivers com suporte para um servidor, use a função [**DeletePrinterDriverEx**](deleteprinterdriverex.md) .

**DeletePrinterDriver** excluirá um driver somente se nenhuma versão do driver estiver em uso para o ambiente especificado. [**DeletePrinterDriverEx**](deleteprinterdriverex.md) pode excluir versões específicas do driver.

## <a name="syntax"></a>Sintaxe


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pname* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do servidor do qual o driver deve ser excluído. Se esse parâmetro for **nulo**, o nome do driver de impressora será removido localmente.

</dd> <dt>

*pEnvironment* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o ambiente do qual o driver deve ser excluído (por exemplo, Windows x86, Windows IA64 ou Windows x64). Se esse parâmetro for **nulo**, o nome do driver será excluído do ambiente atual do aplicativo de chamada e do computador cliente (não do aplicativo de destino e do servidor de impressão).

</dd> <dt>

*pDriverName* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres terminada em nulo que especifica o nome do driver que deve ser excluído.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

O chamador deve ter o [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

A função **DeletePrinterDriver** não exclui os arquivos associados, ele simplesmente remove o nome do driver da lista retornada pela função [**EnumPrinterDrivers**](enumprinterdrivers.md) .

Antes de chamar **DeletePrinterDriver**, você deve excluir todos os objetos de impressora que usam o driver de impressora.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **DeletePrinterDriverW** (Unicode) e **DeletePrinterDriverA** (ANSI)<br/>                         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterDriverEx**](deleteprinterdriverex.md)
</dt> <dt>

[**EnumPrinterDrivers**](enumprinterdrivers.md)
</dt> </dl>

 

