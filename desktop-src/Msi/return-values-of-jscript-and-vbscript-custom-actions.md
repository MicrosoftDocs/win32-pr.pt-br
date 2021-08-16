---
description: Ações personalizadas escritas JScript ou Visual Basic, a VBScript (Scripting Edition) pode chamar uma função opcional. Essas funções devem retornar um dos valores mostrados na tabela a seguir.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Retornar valores de JScript e ações personalizadas do VBScript
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50a2b225c59b0e4d1787f2eaceeb094d6fb2abe7f9d9600822b6295ef2dd273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626086"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a>Retornar valores de JScript e ações personalizadas do VBScript

Ações personalizadas escritas JScript ou Visual Basic, a VBScript (Scripting Edition) pode chamar uma função opcional. Essas funções devem retornar um dos valores mostrados na tabela a seguir.



| Valor retornado              | Valor        | Descrição                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| msiDoActionStatusNoAction | 0            | Ação não executada.                                                                                       |
| msiDoActionStatusSuccess  | IDOK = 1     | Ação concluída com êxito.                                                                             |
| msiDoActionStatusUserExit | IDCANCEL = 2 | Encerramento prematura por usuário.                                                                             |
| msiDoActionStatusFailure  | IDABORT = 3  | Erro irrecuperável. Retornado se houver um erro durante a análise ou execução do JScript ou VBScript. |
| msiDoActionStatusSuspend  | IDRETRY = 4  | Sequência suspensa a ser retomada posteriormente.                                                                    |
| msiDoActionStatusFinished | IDIGNORE = 5 | Ignore as ações restantes. Não é um erro.                                                                      |



 

Observe que Windows Instalador converte os valores de retorno de todas as ações quando grava o valor de retorno no arquivo de log. Por exemplo, se o valor retornado da ação aparecer como 1 (um) no arquivo de log, isso significa que a ação retornou msiDoActionStatusSuccess. Para obter mais informações sobre essa tradução, consulte [Registro em log de valores de retorno de ação](logging-of-action-return-values.md).

Para retornar um valor diferente do sucesso de uma ação personalizada de script, você deve usar um destino de função para a ação personalizada. A função de destino é especificada na coluna Destino da [Tabela CustomAction](customaction-table.md).

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



Se esse VBScript fosse [](binary-table.md) inserido na tabela Binária do pacote de instalação como MyCA.vbs, a entrada [Tabela CustomAction](customaction-table.md) para o script seria a seguinte:



| Ação         | Tipo | Fonte   | Destino       |
|----------------|------|----------|--------------|
| MyCustomAction | 6    | MyCA.vbs | MyVBScriptCA |



 

 

 



