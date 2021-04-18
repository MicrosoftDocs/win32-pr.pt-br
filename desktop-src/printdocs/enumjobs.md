---
description: A função EnumJobs recupera informações sobre um conjunto especificado de trabalhos de impressão para uma impressora especificada.
ms.assetid: 1cf429ea-b40e-4063-b6de-c43b7b87f3d3
title: Função EnumJobs (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumJobs
- EnumJobsA
- EnumJobsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 174f58ba3fb1012e6ff46612fe312579969e6945
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170507"
---
# <a name="enumjobs-function"></a>Função EnumJobs

A função **EnumJobs** recupera informações sobre um conjunto especificado de trabalhos de impressão para uma impressora especificada.

## <a name="syntax"></a>Sintaxe


```C++
BOOL EnumJobs(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   FirstJob,
  _In_  DWORD   NoJobs,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pJob,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hPrinter* \[ no\]
</dt> <dd>

Um identificador para o objeto de impressora cujos trabalhos de impressão a função enumera. Use a função [**OpenPrinter**](openprinter.md) ou [**addprintr**](addprinter.md) para recuperar um identificador de impressora.

</dd> <dt>

*FirstJob* \[ no\]
</dt> <dd>

A posição de base zero dentro da fila de impressão do primeiro trabalho de impressão a ser enumerado. Por exemplo, um valor de 0 especifica que a enumeração deve começar no primeiro trabalho de impressão na fila de impressão; um valor de 9 especifica que a enumeração deve começar no décimo trabalho de impressão na fila de impressão.

</dd> <dt>

*Nojobs* \[ no\]
</dt> <dd>

O número total de trabalhos de impressão a serem enumerados.

</dd> <dt>

*Nível* \[ do no\]
</dt> <dd>

O tipo de informação retornado no buffer *pJob* .



| Valor                                                                                                | Significado                                                                              |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | *pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 1**](job-info-1.md)<br/> |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | *pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 2**](job-info-2.md)<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | *pJob* recebe uma matriz de estruturas de [**informações de trabalho \_ \_ 3**](job-info-3.md)<br/> |



 

</dd> <dt>

*pJob* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe uma matriz das [**estruturas \_ informações \_ do trabalho 1**](job-info-1.md), informações do [**trabalho \_ \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 3**](job-info-3.md) . O buffer deve ser grande o suficiente para receber a matriz de estruturas e quaisquer cadeias de caracteres ou outros dados aos quais os membros da estrutura apontam.

Para determinar o tamanho do buffer necessário, chame **EnumJobs** com *cbBuf* definido como zero. **EnumJobs** falha, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna \_ um buffer insuficiente de erro \_ e o parâmetro *pcbNeeded* retorna o tamanho, em bytes, do buffer necessário para manter a matriz de estruturas e seus dados.

</dd> <dt>

*cbBuf* \[ no\]
</dt> <dd>

O tamanho, em bytes, do buffer *pJob* .

</dd> <dt>

*pcbNeeded* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de bytes copiados se a função for realizada com sucesso. Se a função falhar, a variável receberá o número de bytes necessários.

</dd> <dt>

*pcReturned* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável que recebe o número de estruturas de informações do trabalho [**\_ \_ 1**](job-info-1.md), [**informações do trabalho \_ \_ 2**](job-info-2.md)ou [**informações do trabalho \_ \_ 3**](job-info-3.md) retornadas no buffer *pJob* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, o valor de retorno será um valor diferente de zero.

Se a função falhar, o valor retornado será zero.

## <a name="remarks"></a>Comentários

> [!Note]  
> Essa é uma função de bloqueio ou síncrona e pode não retornar imediatamente. A rapidez com que essa função retorna depende de fatores de tempo de execução, como status de rede, configuração de servidor de impressão e fatores de implementação de driver de impressora que são difíceis de prever ao escrever um aplicativo. Chamar essa função de um thread que gerencia a interação com a interface do usuário pode fazer com que o aplicativo pareça não responder.

 

A [**estrutura \_ informações \_ do trabalho 1**](job-info-1.md) contém informações gerais de trabalho de impressão; a estrutura [**informações do trabalho \_ \_ 2**](job-info-2.md) tem informações muito mais detalhadas. A [**estrutura \_ informações \_ do trabalho 3**](job-info-3.md) contém informações sobre como os trabalhos são vinculados.

Para determinar o número de trabalhos de impressão na fila de impressora, chame a função [**Getprinter**](getprinter.md) com o parâmetro *Level* definido como 2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Winspool. h (incluir Windows. h)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Nomes Unicode e ANSI<br/>   | **EnumJobsW** (Unicode) e **EnumJobsA** (ANSI)<br/>                                               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Impressão](printdocs-printing.md)
</dt> <dt>

[Funções da API do Spooler de impressão](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**Getprinter**](getprinter.md)
</dt> <dt>

[**Informações do trabalho \_ \_ 1**](job-info-1.md)
</dt> <dt>

[**Informações do trabalho \_ \_ 2**](job-info-2.md)
</dt> <dt>

[**Informações do trabalho \_ \_ 3**](job-info-3.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

