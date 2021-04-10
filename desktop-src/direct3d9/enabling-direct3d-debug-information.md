---
description: Você está tentando encontrar mais informações sobre objetos do Direct3D durante a depuração? Por exemplo, a captura de tela a seguir mostra o que você normalmente vê quando examina uma interface do Direct3D na janela Watch.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Habilitando informações de depuração do Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087217"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a>Habilitando informações de depuração do Direct3D (Direct3D 9)

Você está tentando encontrar mais informações sobre objetos do Direct3D durante a depuração? Por exemplo, a captura de tela a seguir mostra o que você normalmente vê quando examina uma interface do Direct3D na janela Watch.

![captura de tela de uma interface do Direct3D na janela Watch](images/d3d-debug-info1.png)

Você pode habilitar os principais objetos de depuração para que um objeto espelhado que contém todas as propriedades do objeto possa ser exibido na janela Watch. Basta incluir a seguinte \# definição no seu código antes do arquivo d3d9. h:


```
#define D3D_DEBUG_INFO
```



Para habilitar as informações de depuração, a \# definição deve ser criada antes do arquivo d3d9. h (qualquer programa que use DXUT habilitará automaticamente \_ \_ as informações de depuração do D3D quando o programa for compilado para depuração). Se você estiver executando um exemplo de SDK, poderá ver isso em DXStdAfx. h (que afeta todos os exemplos de C++). Você também deve estar executando o tempo de execução de debug Direct3D (que pode ser habilitado no painel de controle, se necessário).

Aqui está um exemplo usando o [exemplo BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).

1.  Adicione o \# definir ao arquivo Dxstdafx. h antes da linha 37.
2.  Compilar um projeto de depuração.
3.  Definir um ponto de interrupção na linha 307 em BasicHLSL. cpp
4.  Execute o depurador.

A captura de tela a seguir mostra o tipo de informações detalhadas que você pode obter sobre um objeto de textura de Direct3D na janela Watch.

![captura de tela de um objeto de textura de Direct3D na janela Watch](images/d3d-debug-info2.png)

> [!Note]
>
> Os nomes de propriedade de objeto são visíveis e os valores só são corretos quando o tempo de execução de depuração está habilitado. Ao executar no tempo de execução de varejo, os valores são inválidos.

 

## <a name="use-the-call-stack-for-extended-debug"></a>Usar a pilha de chamadas para depuração estendida

Com a depuração do Direct3D habilitada, você também pode examinar uma pilha de chamadas cada vez que um objeto é criado. Isso tornará seu aplicativo muito lento, mas poderá ser usado para verificar se há vazamentos de recursos. Para gravar a pilha de chamadas, defina a seguinte chave do registro como 1:


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



Criar seu aplicativo com depuração habilitada lhe dará acesso a essa variável adicional:


```
  LPCWSTR CreationCallStack;
```



Essa variável armazenará a pilha de chamadas cada vez que um objeto for criado. Isso tornará seu aplicativo muito lento, mas poderá ser usado para depurar vazamentos de recursos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dicas de programação](programming-tips.md)
</dt> </dl>

 

 



