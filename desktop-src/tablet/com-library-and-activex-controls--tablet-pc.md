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
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="0c317-103">Biblioteca COM e controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="0c317-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="0c317-104">Esta seção descreve como configurar seu ambiente para usar as bibliotecas COM da plataforma Tablet PC em C++.</span><span class="sxs-lookup"><span data-stu-id="0c317-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="0c317-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="0c317-105">Microsoft Visual C++</span></span>

<span data-ttu-id="0c317-106">Para criar aplicativos de Tablet PC no Visual C++, você precisa atualizar as variáveis de ambiente do sistema, configurar as opções de diretório para o Visual Studio e acessar as interfaces do Tablet PC em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="0c317-107">Para atualizar as variáveis de ambiente, siga as instruções fornecidas pelo SDK do Windows para adicionar as variáveis de ambiente ao Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0c317-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="0c317-108">Acessando as interfaces do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="0c317-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="0c317-109">Para acessar as interfaces do Tablet PC, você deve incluir os arquivos Msinkaut. h e Msinkaut \_ i. c em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="0c317-110">Você também pode usar a seguinte diretiva de importação em vez das \# instruções include listadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0c317-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0c317-111">Para acessar as interfaces InkAnalysis, você deve incluir os arquivos IACom. h e IACom \_ i. c em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="0c317-112">Você também pode usar a seguinte diretiva de importação em vez das \# instruções include listadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0c317-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0c317-113">Para acessar as interfaces [**InkDivider**](inkdivider-class.md) , você deve incluir os \_ arquivos msinkaut15 i. c e msinkaut15. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="0c317-114">InkDivider foi substituído pelas APIs de análise de tinta.</span><span class="sxs-lookup"><span data-stu-id="0c317-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="0c317-115">Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.</span><span class="sxs-lookup"><span data-stu-id="0c317-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0c317-116">Para acessar as interfaces [**PenInputPanel**](peninputpanel-class.md) , você deve incluir os \_ arquivos PenInputPanel i. c e PenInputPanel. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="0c317-117">Você também pode usar a seguinte diretiva de importação em vez das \# instruções include.</span><span class="sxs-lookup"><span data-stu-id="0c317-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="0c317-118">As APIs PenInputPanel foram substituídas no Windows Vista pelas novas interfaces do painel de entrada de texto.</span><span class="sxs-lookup"><span data-stu-id="0c317-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="0c317-119">Para acessar as interfaces de controle [InkEdit](inkedit-control-reference.md) , você deve incluir os arquivos Inked. h e Inked \_ i. c em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="0c317-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="0c317-120">Como alternativa, você pode \# importar o arquivo de InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="0c317-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



