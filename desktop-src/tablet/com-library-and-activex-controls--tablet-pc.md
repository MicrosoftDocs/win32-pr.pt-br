---
description: Esta seção descreve como configurar seu ambiente para usar as bibliotecas COM da plataforma Tablet PC em C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Biblioteca COM e controles ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813661"
---
# <a name="com-library-and-activex-controls"></a>Biblioteca COM e controles ActiveX

Esta seção descreve como configurar seu ambiente para usar as bibliotecas COM da plataforma Tablet PC em C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Para criar aplicativos de Tablet PC no Visual C++, você precisa atualizar as variáveis de ambiente do sistema, configurar as opções de diretório para o Visual Studio e acessar as interfaces do Tablet PC em seu projeto.

Para atualizar as variáveis de ambiente, siga as instruções fornecidas pelo SDK do Windows para adicionar as variáveis de ambiente ao Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Acessando as interfaces do Tablet PC

Para acessar as interfaces do Tablet PC, você deve incluir os arquivos Msinkaut. h e Msinkaut \_ i. c em seu projeto.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include listadas anteriormente.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces InkAnalysis, você deve incluir os arquivos IACom. h e IACom \_ i. c em seu projeto.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include listadas anteriormente.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces [**InkDivider**](inkdivider-class.md) , você deve incluir os \_ arquivos msinkaut15 i. c e msinkaut15. h em seu projeto.

> [!Note]  
> InkDivider foi substituído pelas APIs de análise de tinta.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces [**PenInputPanel**](peninputpanel-class.md) , você deve incluir os \_ arquivos PenInputPanel i. c e PenInputPanel. h em seu projeto.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> As APIs PenInputPanel foram substituídas no Windows Vista pelas novas interfaces do painel de entrada de texto.

 

Para acessar as interfaces de controle [InkEdit](inkedit-control-reference.md) , você deve incluir os arquivos Inked. h e Inked \_ i. c em seu projeto.


```C++
#include <inked.h>
#include <inked_i.c>
```



Como alternativa, você pode \# importar o arquivo de InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



