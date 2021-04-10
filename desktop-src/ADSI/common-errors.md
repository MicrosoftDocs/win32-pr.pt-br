---
title: Erros comuns (ADSI)
description: Todos os erros específicos de ADSI têm uma forma hexadecimal de 80005xxx. Os códigos de erro mais comuns encontrados são descritos na tabela a seguir.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104293686"
---
# <a name="common-errors-adsi"></a>Erros comuns (ADSI)

Todos os erros específicos de ADSI têm uma forma hexadecimal de 80005xxx. Os códigos de erro mais comuns encontrados são descritos na tabela a seguir.



| Código de erro hexadecimal ADSI | Descrição                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| 80005000<br/> | Um nome de caminho ADSI inválido foi passado. Esse erro resulta da transmissão de um ADsPath mal formado para **GetObject** durante a associação a um objeto.<br/> |
| 8000500D<br/> | A propriedade ADSI não pode ser encontrada no cache de propriedades.<br/>                                                                                 |
| 8000500E<br/> | O objeto ADSI existe. Se você tentar criar um objeto ADSI com o mesmo nome de um objeto ADSI existente, esse erro ocorrerá.<br/>    |



 

Para obter uma lista completa de códigos de erro ADSI, consulte [códigos de erro genéricos da ADSI](generic-adsi-error-codes.md).

## <a name="com-errors"></a>Erros COM

Como a ADSI é composta de objetos COM, ela retornará códigos de erro padrão COM. A tabela a seguir lista os códigos de erro COM mais comumente encontrados na programação ADSI.



| Código de erro HEX COM  | Descrição                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 80004005<br/> | Erro não especificado. A causa da falha do objeto COM é indeterminada pela ADSI. <br/>                                  |
| 800041E4<br/> | Objeto não localizado. Esse erro é basicamente causado devido à grafia incorreta da cadeia de caracteres ADsPath ao associar a um objeto.<br/> |



 

Consulte [códigos de erro com genéricos](generic-com-error-codes.md) para obter mais alguns exemplos de erros com que podem ocorrer na programação ADSI.

## <a name="win32-errors"></a>Erros do Win32

Qualquer código de erro do formato hexadecimal 8007xxxx é um código de erro Win32 padrão. Se você converter os últimos quatro dígitos de hexadecimal para decimal, poderá acessar o erro na linha de comando do Windows 2000:

**NET HELPMSG <number>**

Na linha de comando acima, " &lt; número &gt; " é o número decimal obtido pela conversão dos últimos quatro dígitos do código de erro de hexadecimal. Essa linha de comando fornecerá uma descrição mais útil do erro do Win32, que pode ser de grande ajuda para depurar seu script.

 

 





