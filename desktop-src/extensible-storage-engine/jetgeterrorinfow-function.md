---
description: 'Saiba mais sobre: Função JetGetErrorInfoW'
title: Função JetGetErrorInfoW
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f459d98ee2cc3c0bb1b57eb5cd4fb630d076836b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468973"
---
# <a name="jetgeterrorinfow-function"></a>Função JetGetErrorInfoW


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="jetgeterrorinfow-function"></a>Função JetGetErrorInfoW

A **função JetGetErrorInfoW** BAS_ do mecanismo de banco de dados.

Observação: esta documentação baseia-se em uma versão preliminar do Mecanismo Armazenamento Extensível. Essas informações estão sujeitas a alterações.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Parâmetros

*pvContext*

O valor de contexto ou erro para o qual as informações de erro estendidas são necessárias. O valor passado depende do valor *do parâmetro InfoLevel.*

*pvResult*

Um ponteiro para um buffer que receberá as informações. O tipo do buffer depende do valor *do parâmetro InfoLevel.* O chamador deve ser configurado para alinhar o buffer adequadamente.

*cbMax*

O tamanho máximo da estrutura *pvResult* que é passada.

*InfoLevel*

O tipo de informação que será recuperado para as informações/contexto de erro é especificado pelo *parâmetro pvContext.* O formato dos dados armazenados em *pvResult* depende de *InfoLevel.*

A tabela a seguir lista os valores possíveis para esse parâmetro.


| <p>Valor</p> | <p>Significado</p> | 
|--------------|----------------|
| <p>JET_ErrorInfoSpecificErr</p> | <p><em>pvContext</em> é interpretado como um código <a href="gg269297(v=exchg.10).md">JET_ERR</a>/error, <em>pvResult</em> é interpretado como <a href="hh475861(v=exchg.10).md">um JET_ERRINFOBASIC_W</a>e os campos da estrutura <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> são preenchidos adequadamente.</p> | 



*grbit*

Reservado.

### <a name="return-value"></a>Valor Retornado

Essa função retorna o [JET_ERR](./extensible-storage-engine-error-codes.md) de dados com um dos códigos de retorno listados na tabela a seguir. Para obter mais informações sobre os possíveis erros de ESE, consulte [Extensible Armazenamento Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).


| <p>Código de retorno</p> | <p>Descrição</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>A operação foi concluída com sucesso.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Um dos parâmetros fornecidos contém um valor inesperado ou contém um valor que não faz sentido quando combinado com o valor de outro parâmetro. Isso pode acontecer para <strong>JetGetErrorInfo</strong> quando ocorre o seguinte:</p><ul><li><p>O valor do <em>parâmetro InfoLevel</em> especificado é inválido.</p></li><li><p>O valor <em>de grbit</em> especificado é inválido.</p></li><li><p>O valor <em>cbMax</em> do parâmetro <em>pvResult</em> especificado é menor que o tamanho necessário para a saída desse <em>parâmetro InfoLevel.</em></p></li><li><p>Para <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, o <a href="gg294092(v=exchg.10).md">JET_ERR</a> valor passado é desconhecido para o mecanismo.</p></li></ul> | 
| <p>JET_errDisabledFunctionality</p> | <p>Se essa SKU do Windows não dá suporte a essa função, esse erro será retornado.</p> | 



Em caso de êxito, o buffer de saída apropriado para o contexto/valor de erro solicitado será definido como as informações de erro estendidas solicitadas.

Em caso de falha, o estado dos buffers de saída será indefinido.

### <a name="remarks"></a>Comentários

A [função JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) e JET_ERRCAT de constantes contêm [documentação](./jet-errcat.md) sobre as informações de erro estendidas retornadas para *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Requisitos


| | | <p><strong>Cliente</strong></p> | <p>Requer Windows 8.</p> | | <p><strong>Servidor</strong></p> | <p>Requer Windows 8 Server.</p> | | <p><strong>Cabeçalho</strong></p> | <p>Declarado em Esent.h.</p> | | <p><strong>Biblioteca</strong></p> | <p>Use ESENT.lib.</p> | | <p><strong>DLL</strong></p> | <p>Requer ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Observação: somente <strong>o JetGetErrorInfoW</strong> (Unicode) é implementado. Essa API não tem uma versão A (ANSI).</p> | 

