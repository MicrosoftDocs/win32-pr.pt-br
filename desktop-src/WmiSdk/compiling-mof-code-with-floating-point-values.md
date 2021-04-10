---
description: O compilador MOF aceita um valor de ponto flutuante especificado para uma propriedade de ponto não flutuante. O valor é arredondado para cima ou para baixo e armazenado como um número de ponto não-flutuante. Essa situação pode causar alguns resultados inesperados.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilando código MOF com valores de Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170617"
---
# <a name="compiling-mof-code-with-floating-point-values"></a><span data-ttu-id="729b8-105">Compilando código MOF com valores de Floating-Point</span><span class="sxs-lookup"><span data-stu-id="729b8-105">Compiling MOF Code with Floating-Point Values</span></span>

<span data-ttu-id="729b8-106">O compilador MOF aceita um valor de ponto flutuante especificado para uma propriedade de ponto não flutuante.</span><span class="sxs-lookup"><span data-stu-id="729b8-106">The MOF compiler accepts a floating-point value specified for a nonfloating-point property.</span></span> <span data-ttu-id="729b8-107">O valor é arredondado para cima ou para baixo e armazenado como um número de ponto não-flutuante.</span><span class="sxs-lookup"><span data-stu-id="729b8-107">The value is rounded up or down and stored as a nonfloating-point number.</span></span> <span data-ttu-id="729b8-108">Essa situação pode causar alguns resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="729b8-108">This situation can cause some unexpected results.</span></span>

<span data-ttu-id="729b8-109">O exemplo de código MOF a seguir define uma classe chamada **ABC** em um namespace chamado "Test".</span><span class="sxs-lookup"><span data-stu-id="729b8-109">The following MOF code example defines a class called **abc** in a namespace called "Test".</span></span> <span data-ttu-id="729b8-110">Esse código MOF compila sem erros, mas você não pode consultar o valor de ponto flutuante definido para a propriedade **exampleUint16** na instância que esse código cria.</span><span class="sxs-lookup"><span data-stu-id="729b8-110">This MOF code compiles without errors, but you cannot query for the floating-point value defined for the property **exampleUint16** in the instance this code creates.</span></span>

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

<span data-ttu-id="729b8-111">Se você emitir a consulta a seguir, obterá um código de erro que indica uma consulta inválida.</span><span class="sxs-lookup"><span data-stu-id="729b8-111">If you issue the following query, you get an error code that indicates an invalid query.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



<span data-ttu-id="729b8-112">No entanto, a consulta a seguir localiza a instância indicada.</span><span class="sxs-lookup"><span data-stu-id="729b8-112">However, the following query finds the indicated instance.</span></span>


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a><span data-ttu-id="729b8-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="729b8-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="729b8-114">Compilando arquivos MOF</span><span class="sxs-lookup"><span data-stu-id="729b8-114">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="729b8-115">**Mofcomp**</span><span class="sxs-lookup"><span data-stu-id="729b8-115">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="729b8-116">Comandos de pré-processador</span><span class="sxs-lookup"><span data-stu-id="729b8-116">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



