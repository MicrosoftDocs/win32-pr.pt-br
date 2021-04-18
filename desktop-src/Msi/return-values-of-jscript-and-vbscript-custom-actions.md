---
description: Ações personalizadas escritas em JScript ou Visual Basic, Scripting Edition (VBScript) podem chamar uma função opcional. Essas funções devem retornar um dos valores mostrados na tabela a seguir.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Valores de retorno de ações personalizadas do JScript e do VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753260"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Valores de retorno de ações personalizadas do JScript e do VBScript

Ações personalizadas escritas em JScript ou Visual Basic, Scripting Edition (VBScript) podem chamar uma função opcional. Essas funções devem retornar um dos valores mostrados na tabela a seguir.



| Retornar valor              | Valor        | Descrição                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Ação não executada.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Ação concluída com êxito.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Encerramento prematuro pelo usuário.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Erro irrecuperável. Retornado se houver um erro durante a análise ou execução do JScript ou VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Sequência suspensa a ser retomada mais tarde.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Ignorar as ações restantes. Não é um erro.                                                                      |



 

Observe que Windows Installer converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log. Por exemplo, se o valor de retorno da ação aparecer como 1 (um) no arquivo de log, isso significa que a ação retornou msiDoActionStatusSuccess. Para obter mais informações sobre essa conversão, consulte [log de valores de retorno de ação](logging-of-action-return-values.md).

Para retornar um valor diferente de êxito de uma ação personalizada de script, você deve usar um destino de função para a ação personalizada. A função de destino é especificada na coluna de destino da [tabela CustomAction](customaction-table.md).

O exemplo de script a seguir mostra como retornar êxito ou falha de uma ação personalizada do VBScript.


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



Se esse VBScript tiver sido inserido na [tabela binária](binary-table.md) do pacote de instalação como MyCA.vbs, a entrada da [tabela CustomAction](customaction-table.md) para o script será a seguinte:



| Ação         | Tipo | Fonte   | Destino       |
|----------------|------|----------|--------------|
| Mycustomizable | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



