---
description: uma das principais ferramentas do Instrumentação de Gerenciamento do Windows (WMI) é a capacidade de consultar o repositório WMI quanto a informações de classe e instância.
ms.assetid: 0cceda42-fba0-4a08-90dd-43f022d0be41
ms.tgt_platform: multiple
title: Consultando o WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc9cd51946bad1df482bb286c538e38bba8e2b3337776e3cd62e0a0da652574
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817534"
---
# <a name="querying-wmi"></a>Consultando o WMI

uma das principais ferramentas do Instrumentação de Gerenciamento do Windows (WMI) é a capacidade de consultar o repositório WMI quanto a informações de classe e instância. Por exemplo, você pode solicitar que o WMI retorne todos os objetos que representam eventos de desligamento do seu sistema de desktop. Você também pode recuperar dados de classe, instância ou esquema. A tabela a seguir lista os diferentes tipos de consultas que você pode fazer.



| Tópico                                                                | Descrição                                                                                                                                                                                      |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Invocando uma consulta síncrona](invoking-a-synchronous-query.md)     | Descreve como manter um link com o WMI em todo o processo de consulta. As consultas síncronas são válidas para consultas pequenas ou consultas a um sistema local.<br/>                                  |
| [Invocando uma consulta assíncrona](invoking-an-asynchronous-query.md) | Descreve como configurar um processo separado para receber consultas. As consultas assíncronas são mais complexas e fornecem um nível mais baixo de segurança, mas geralmente melhoram o desempenho do sistema.<br/> |



 

Além de consultar o repositório WMI, você também pode usar o [*linguagem WQL (WQL)*](gloss-w.md) para rotear eventos de notificação para seu aplicativo. Para obter mais informações, consulte [recebendo um evento WMI](receiving-a-wmi-event.md).

> [!Note]
>
> Para consultar o WMI corretamente, você deve ter uma boa compreensão do WQL. Uma consulta incorreta, muito complexa ou inadequada pode fazer com que o processador de consultas retorne um erro ou resultados inesperados. Para obter um guia abrangente da WQL, consulte [consultando com WQL](querying-with-wql.md).
>
> Há limites para o número de palavras-chave **and** e **or** que podem ser usadas em consultas WQL. Grandes números de palavras-chave WQL usadas em uma consulta complexa podem fazer com que o WMI retorne o código de erro de **\_ \_ \_ violação E de cota de WBEM** como um valor **HRESULT** . O limite de palavras-chave WQL depende da complexidade da consulta.
>
> Ao consultar valores de propriedade com um tipo de dados **UInt64** ou **sint64** em uma linguagem de script como o VBScript, o WMI retorna valores de cadeia de caracteres. Resultados inesperados podem ocorrer ao comparar esses valores, pois a comparação de cadeias de caracteres retorna resultados diferentes de comparação de números. Por exemplo, "10000000000" é menor que "9" ao comparar cadeias de caracteres e 9 é menor que 10000000000 ao comparar números. Para evitar confusão, você deve usar o método [CDbl](/previous-versions//ftekwwt0(v=vs.85)) no VBScript quando as propriedades do tipo **UInt64** ou **SINT64** são recuperadas do WMI.

 

> [!Note]  

 

Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

 

