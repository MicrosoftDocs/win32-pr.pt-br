---
description: O instalador fornece funções que manipulam os registros em um banco de dados de instalação. Essas funções podem ser usadas em conjunto com as funções descritas em trabalhando com consultas para fazer alterações reais em um banco de dados.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Trabalhando com registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748561"
---
# <a name="working-with-records"></a><span data-ttu-id="e936d-104">Trabalhando com registros</span><span class="sxs-lookup"><span data-stu-id="e936d-104">Working with Records</span></span>

<span data-ttu-id="e936d-105">O instalador fornece funções que manipulam os registros em um banco de dados de instalação.</span><span class="sxs-lookup"><span data-stu-id="e936d-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="e936d-106">Essas funções podem ser usadas em conjunto com as funções descritas em [trabalhando com consultas](working-with-queries.md) para fazer alterações reais em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="e936d-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="e936d-107">As funções a seguir criam ou removem registros:</span><span class="sxs-lookup"><span data-stu-id="e936d-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="e936d-108">Para criar um novo registro para um banco de dados, chame a função [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .</span><span class="sxs-lookup"><span data-stu-id="e936d-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="e936d-109">Para limpar dados de um registro, defina cada campo como nulo chamando a função [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .</span><span class="sxs-lookup"><span data-stu-id="e936d-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="e936d-110">As funções a seguir preenchem campos especificados de registros:</span><span class="sxs-lookup"><span data-stu-id="e936d-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="e936d-111">Para definir um registro como um inteiro, chame a função [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .</span><span class="sxs-lookup"><span data-stu-id="e936d-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="e936d-112">Para definir um registro para uma cadeia de caracteres, chame a função [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .</span><span class="sxs-lookup"><span data-stu-id="e936d-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="e936d-113">Para inserir um arquivo inteiro em um campo de fluxo, chame a função [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .</span><span class="sxs-lookup"><span data-stu-id="e936d-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="e936d-114">As funções a seguir lêem valores de campos especificados de registros:</span><span class="sxs-lookup"><span data-stu-id="e936d-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="e936d-115">Para ler um valor inteiro de um campo, chame a função [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .</span><span class="sxs-lookup"><span data-stu-id="e936d-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="e936d-116">Para recuperar um valor de cadeia de caracteres, chame a função [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .</span><span class="sxs-lookup"><span data-stu-id="e936d-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="e936d-117">Para obter um fluxo, chame a função [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .</span><span class="sxs-lookup"><span data-stu-id="e936d-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="e936d-118">Para determinar se um determinado campo de um registro é nulo, chame a função [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .</span><span class="sxs-lookup"><span data-stu-id="e936d-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="e936d-119">As funções a seguir são funções de registro informativo:</span><span class="sxs-lookup"><span data-stu-id="e936d-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="e936d-120">Para obter o número de campos que um registro contém, chame a função [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .</span><span class="sxs-lookup"><span data-stu-id="e936d-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="e936d-121">Para obter o tamanho de um campo, chame a função [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) .</span><span class="sxs-lookup"><span data-stu-id="e936d-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="e936d-122">O valor de retorno de **MsiRecordDataSize** é sensível ao tipo de campo.</span><span class="sxs-lookup"><span data-stu-id="e936d-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



