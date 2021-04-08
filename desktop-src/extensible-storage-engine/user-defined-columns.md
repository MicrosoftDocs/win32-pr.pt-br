---
description: 'Saiba mais sobre: colunas definidas pelo usuário'
title: Colunas definidas pelo usuário
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010745"
---
# <a name="user-defined-columns"></a><span data-ttu-id="4bd11-103">Colunas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4bd11-103">User Defined Columns</span></span>


<span data-ttu-id="4bd11-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="4bd11-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="4bd11-105">Colunas definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="4bd11-105">User Defined Columns</span></span>

<span data-ttu-id="4bd11-106">As colunas definidas pelo usuário são colunas cujos valores padrão são fornecidos por uma função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4bd11-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="4bd11-107">Essas colunas são sempre marcadas e definidas com o valor calculado pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="4bd11-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="4bd11-108">Esse valor deve ser estável para cada linha na tabela.</span><span class="sxs-lookup"><span data-stu-id="4bd11-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="4bd11-109">A função de retorno de chamada só é usada quando o aplicativo ou o mecanismo de banco de dados precisa ler o valor da coluna para uma determinada linha.</span><span class="sxs-lookup"><span data-stu-id="4bd11-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="4bd11-110">O aplicativo tem a opção de substituir o valor padrão e definir um valor específico na coluna.</span><span class="sxs-lookup"><span data-stu-id="4bd11-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="4bd11-111">Quando o valor padrão é substituído nas colunas, ele usa o espaço na linha; caso contrário, as colunas padrão definidas pelo usuário não usam espaço no registro.</span><span class="sxs-lookup"><span data-stu-id="4bd11-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="4bd11-112">A opção padrões definidos pelo usuário é definida no membro **grbit** da estrutura [JET_COLUMNDEF](./jet-columndef-structure.md) na chamada de [JetAddColumn](./jetaddcolumn-function.md).</span><span class="sxs-lookup"><span data-stu-id="4bd11-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="4bd11-113">O parâmetro *pvDefault* da função [JetAddColumn](./jetaddcolumn-function.md) aponta para uma estrutura de [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) , que contém o nome da função de retorno de chamada no membro **szCallback** , e os dados que são passados para o retorno de chamada no membro **pbUserData** .</span><span class="sxs-lookup"><span data-stu-id="4bd11-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
