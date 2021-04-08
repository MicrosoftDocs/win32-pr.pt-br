---
description: Verifica a assinatura de um arquivo assinado e Obtém o valor de hash e o identificador do algoritmo para o arquivo.
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: Função WTHelperGetFileHash
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921844"
---
# <a name="wthelpergetfilehash-function"></a>Função WTHelperGetFileHash

\[A função **WTHelperGetFileHash** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]

A função **WTHelperGetFileHash** verifica a assinatura de um arquivo assinado e Obtém o valor de hash e o identificador de algoritmo para o arquivo.

> [!Note]  
> Essa função não é declarada em um arquivo de cabeçalho publicado. Para usar essa função, declare-a no formato exato mostrado. Essa função também não tem biblioteca de importação associada. Você deve usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Wintrust.dll.

 

## <a name="syntax"></a>Sintaxe


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszFilename* \[ no\]
</dt> <dd>

Um ponteiro para uma cadeia de caracteres Unicode terminada em nulo que contém o caminho e o nome de arquivo do arquivo para o qual obter o hash.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*pvReserved* \[ entrada, saída, opcional\]
</dt> <dd>

Esse parâmetro não é usado e deve ser **nulo**.

</dd> <dt>

*pbFileHash* \[ out, opcional\]
</dt> <dd>

Um ponteiro para um buffer para receber o valor de hash do arquivo. O parâmetro *pcbFileHash* contém o tamanho desse buffer.

</dd> <dt>

*pcbFileHash* \[ entrada, saída, opcional\]
</dt> <dd>

Um ponteiro para uma variável **DWORD** que, na entrada, contém o tamanho, em bytes, do buffer *pbFileHash* e, na saída, recebe o tamanho, em bytes, do valor de hash.

Para obter o tamanho necessário do valor de hash, passe **NULL** para o parâmetro *pbFileHash* . Essa função coloca o tamanho necessário, em bytes, do valor de hash neste local.

Se o parâmetro *pbFileHash* não for **nulo** e o tamanho não for grande o suficiente para receber o valor de hash, essa função irá inserir o tamanho necessário, em bytes, nesse local e retornará **\_ mais \_ dados de erro**.

</dd> <dt>

*pHashAlgid* \[ out, opcional\]
</dt> <dd>

Um ponteiro para uma variável de [**\_ ID alg**](alg-id.md) para receber o identificador do algoritmo usado para criar o valor de hash. Esse parâmetro poderá ser **nulo** se essas informações não forem necessárias.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um código de status que indica o êxito ou a falha da função.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código de retorno                                                                                               | Descrição                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**êxito do erro \_**</dt> </dl>             | O arquivo está assinado e a assinatura foi verificada.<br/>                                                                                        |
| <dl> <dt>**ERRO de \_ mais \_ dados**</dt> </dl>          | O parâmetro *pbFileHash* não é **nulo** e o tamanho especificado pelo parâmetro *pcbFileHash* não é grande o suficiente para receber o hash.<br/> |
| <dl> <dt>**ERRO \_ de \_ memória insuficiente \_**</dt> </dl> | Ocorreu uma falha de alocação de memória.<br/>                                                                                                      |
| <dl> <dt>**CONFIAR \_ E \_ má \_ Digest**</dt> </dl>      | A assinatura do arquivo não foi verificada.<br/>                                                                                                |
| <dl> <dt>**CONFIAR \_ E \_ noassinatura**</dt> </dl>      | O arquivo não foi assinado ou tinha uma assinatura que não é válida.<br/>                                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Wintrust.dll</dt> </dl> |



 

 
