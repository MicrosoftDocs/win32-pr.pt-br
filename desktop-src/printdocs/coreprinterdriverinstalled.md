---
description: A função CorePrinterDriverInstalled relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Função CorePrinterDriverInstalled (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011394"
---
# <a name="coreprinterdriverinstalled-function"></a>Função CorePrinterDriverInstalled

A função **CorePrinterDriverInstalled** relata se um driver de impressora principal com um GUID, uma data e uma versão especificados estão instalados.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pszServer* \[ no\]
</dt> <dd>

Ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica o nome do servidor de impressão. Use **NULL** para o computador local.

</dd> <dt>

*pszEnvironment* \[ no\]
</dt> <dd>

Ponteiro para uma constante, Cadeia de caracteres terminada em nulo que especifica a arquitetura do processador (por exemplo, Windows NT x86). Isso pode ser **nulo**.

</dd> <dt>

*CoreDriverGUID* \[ no\]
</dt> <dd>

O GUID do driver de impressora principal.

</dd> <dt>

*ftDriverDate* \[ no\]
</dt> <dd>

A data do driver de impressora principal.

</dd> <dt>

*dwlDriverVersion* \[ no\]
</dt> <dd>

A versão do driver de impressora principal.

</dd> <dt>

*pbDriverInstalled* \[ fora\]
</dt> <dd>

Um ponteiro para **verdadeiro** se o driver ou uma versão mais recente estiver instalado; caso contrário, **false** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será S \_ OK, caso contrário, o **HRESULT** conterá um código de erro.

Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md).

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                      |
| parâmetro<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Nomes Unicode e ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) e **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> </dl>

 

