---
description: Esta seção descreve como configurar seu ambiente para usar as bibliotecas COM da plataforma de Tablet PC no C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Biblioteca COM e controles ActiveX dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bc76f9caa2bcb72fe26ed2e01e251c977f87ce01c12794aad78608d2f5887f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009086"
---
# <a name="com-library-and-activex-controls"></a>Biblioteca COM e controles ActiveX dados

Esta seção descreve como configurar seu ambiente para usar as bibliotecas COM da plataforma de Tablet PC no C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Para criar aplicativos de tablet pc no Visual C++, você precisa atualizar as variáveis de ambiente do sistema, configurar opções de diretório para Visual Studio e acessar as interfaces do Tablet PC em seu projeto.

Para atualizar as variáveis de ambiente, siga as instruções fornecidas pelo SDK do Windows para adicionar as variáveis de ambiente ao Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Acessando as interfaces de tablet pc

Para acessar as interfaces do Tablet PC, você deve incluir os arquivos Msinkaut.h e Msinkaut \_ i.c em seu projeto.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das instruções \# include listadas anteriormente.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces inkAnalysis, você deve incluir arquivos IACom.h e IACom \_ i.c em seu projeto.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das instruções \# include listadas anteriormente.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces [**InkDivider,**](inkdivider-class.md) você deve incluir arquivos msinkaut15 \_ i.c e msinkaut15.h em seu projeto.

> [!Note]  
> InkDivider foi superado pelas APIs de Análise de Tinta.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Para acessar as interfaces [**PenInputPanel,**](peninputpanel-class.md) você deve incluir os arquivos PenInputPanel \_ i.c e PenInputPanel.h em seu projeto.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> As APIs PenInputPanel foram superadas no Windows Vista pelas novas interfaces do Painel de Entrada de Texto.

 

Para acessar as interfaces [do InkEdit](inkedit-control-reference.md) Control, você deve incluir os arquivos Inked.h e Inked \_ i.c em seu projeto.


```C++
#include <inked.h>
#include <inked_i.c>
```



Como alternativa, você pode \# importar o arquivo InkEd.dll dados.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



