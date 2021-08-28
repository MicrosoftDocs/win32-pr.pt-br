---
description: 'Saiba mais sobre: parâmetros de tratamento de erros'
title: Parâmetros de tratamento de erros
TOCTitle: Error Handling Parameters
ms:assetid: 014996a1-5674-40c7-9538-54cae1681fec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269173(v=EXCHG.10)
ms:contentKeyID: 32765476
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 698854aa81ddd7a44fcf58dd250444e657d44a0c
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982009"
---
# <a name="error-handling-parameters"></a>Parâmetros de tratamento de erros


_**Aplica-se a:** Windows | Windows Servidor_

## <a name="error-handling-parameters"></a>Parâmetros de tratamento de erros

Este tópico contém parâmetros que são usados para tratamento de erros.

*JET_paramErrorToString* 70  

Esse parâmetro pode ser usado para converter um [JET_ERR](./jet-err.md) em uma cadeia de caracteres. Isso é feito usando uma chamada especial para [JetGetSystemParameter](./jetgetsystemparameter-function.md) , em que o buffer de saída de inteiro contém o valor de [JET_ERR](./jet-err.md) a ser convertido (como um parâmetro de entrada) e o buffer de saída de cadeia de caracteres retorna a cadeia de caracteres de erro correspondente. A cadeia de caracteres terá uma aparência semelhante a esta: "JET_errSuccess, operação bem-sucedida". A cadeia de caracteres é composta pelo nome simbólico para a cadeia de caracteres, uma vírgula e uma descrição de texto simples do erro. A cadeia de caracteres de descrição pode conter vírgulas. Se o erro não for reconhecido, a cadeia de caracteres será "erro desconhecido, erro desconhecido".

**Observação**  Esse parâmetro é somente leitura.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>Especial</p> | 
| <p>Tipo:</p> | <p>Especial</p> | 
| <p>Intervalo válido:</p> | <p>Especial</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Não</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Não</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Não</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 


*JET_paramExceptionAction*  
98  

Esse parâmetro controla o que acontece quando uma exceção é lançada pelo mecanismo de banco de dados ou pelo código que é chamado pelo mecanismo de banco de dados. quando definido como JET_ExceptionMsgBox, qualquer exceção será lançada para o Windows filtro de exceção sem tratamento. Isso fará com que a exceção seja tratada como uma falha do aplicativo. A intenção é impedir que o código do aplicativo tente detectar erroneamente e ignorar uma exceção gerada pelo mecanismo de banco de dados. Isso não pode ser permitido porque a corrupção do banco de dados pode ocorrer. Se o aplicativo quiser lidar corretamente com essas exceções, a proteção poderá ser desabilitada definindo esse parâmetro como JET_ExceptionNone.


| Rótulo | Valor |
|--------|-------|
| <p>Valor padrão:</p> | <p>JET_ExceptionMsgBox</p> | 
| <p>Tipo:</p> | <p>Integer</p> | 
| <p>Intervalo válido:</p> | <p>JET_ExceptionMsgBox, JET_ExceptionNone</p> | 
| <p>Escopo:</p> | <p>Global</p> | 
| <p>Definir após <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  Não</p><p><strong>Windows Vista:</strong>  Ok</p> | 
| <p>Definir após <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p><strong>Windows 2000, Windows XP e Windows Server 2003:</strong>  Não</p><p><strong>Windows Vista:</strong>  Ok</p> | 
| <p>Afeta o layout físico:</p> | <p>Não</p> | 
| <p>Afeta a confiabilidade:</p> | <p>Sim</p> | 
| <p>Afeta o desempenho:</p> | <p>Não</p> | 
| <p>Afeta os recursos:</p> | <p>Não</p> | 
| <p>Disponibilidade:</p> | <p>Tudo</p> | 


### <a name="requirements"></a>Requisitos


| Requisito | Valor |
|------------|----------|
| <p><strong>Cliente</strong></p> | <p>requer o Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Servidor</strong></p> | <p>requer o Windows server 2008, Windows server 2003 ou Windows servidor 2000.</p> | 
| <p><strong>Cabeçalho</strong></p> | <p>Declarado em ESENT. h.</p> | 


### <a name="see-also"></a>Consulte Também

[Constantes de tratamento de erro](./error-handling-constants.md)  
[códigos de erro do mecanismo de Armazenamento extensível](./extensible-storage-engine-error-codes.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JetInit](./jetinit-function.md)
