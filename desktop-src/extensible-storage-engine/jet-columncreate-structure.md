---
description: 'Saiba mais sobre: estrutura de JET_COLUMNCREATE'
title: Estrutura JET_COLUMNCREATE
TOCTitle: JET_COLUMNCREATE Structure
ms:assetid: 553263a9-7d2c-4bd7-ad77-1dfb6d21ef2c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269252(v=EXCHG.10)
ms:contentKeyID: 32765554
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ee2d9d194a03cf575eb0296163526c1c50301cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770575"
---
# <a name="jet_columncreate-structure"></a><span data-ttu-id="fc51e-103">Estrutura JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="fc51e-103">JET_COLUMNCREATE Structure</span></span>


<span data-ttu-id="fc51e-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="fc51e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_columncreate-structure"></a><span data-ttu-id="fc51e-105">Estrutura JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="fc51e-105">JET_COLUMNCREATE Structure</span></span>

<span data-ttu-id="fc51e-106">A estrutura de **JET_COLUMNCREATE** descreve uma coluna a ser criada em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="fc51e-106">The **JET_COLUMNCREATE** structure describes a column to create in a database.</span></span>

```cpp
    typedef struct tag_JET_COLUMNCREATE {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_COLTYP coltyp;
      unsigned long cbMax;
      JET_GRBIT grbit;
      void* pvDefault;
      unsigned long cbDefault;
      unsigned long cp;
      JET_COLUMNID columnid;
      JET_ERR err;
    } JET_COLUMNCREATE;
```

### <a name="members"></a><span data-ttu-id="fc51e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fc51e-107">Members</span></span>

<span data-ttu-id="fc51e-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="fc51e-108">**cbStruct**</span></span>

<span data-ttu-id="fc51e-109">O tamanho da estrutura, em bytes.</span><span class="sxs-lookup"><span data-stu-id="fc51e-109">The size of the structure, in bytes.</span></span> <span data-ttu-id="fc51e-110">Este campo deve ser inicializado para **sizeof (JET_COLUMNCREATE)**.</span><span class="sxs-lookup"><span data-stu-id="fc51e-110">This field must be initialized to **sizeof( JET_COLUMNCREATE )**.</span></span>

<span data-ttu-id="fc51e-111">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="fc51e-111">**szColumnName**</span></span>

<span data-ttu-id="fc51e-112">O nome da coluna a ser criada.</span><span class="sxs-lookup"><span data-stu-id="fc51e-112">The name of the column to create.</span></span> <span data-ttu-id="fc51e-113">O nome deve atender aos seguintes critérios:</span><span class="sxs-lookup"><span data-stu-id="fc51e-113">The name must meet the following criteria:</span></span>

  - <span data-ttu-id="fc51e-114">Ele deve ter menos de JET_cbNameMost caracteres de comprimento, não incluindo o nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="fc51e-114">It must be fewer than JET_cbNameMost characters in length, not including the terminating NULL.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc51e-115">Ele deve conter caracteres somente dos seguintes conjuntos: 0 a 9, A a Z, a a z e todas as outras pontuações, exceto para ponto de exclamação ( \! ), vírgula (,), colchete de abertura ( \[ ) e colchete de fechamento ( \] ), ou seja, caracteres ASCII 0x20, 0x22 a 0x2d, 0x2F a 0x5A, 0x5c, 0x5d até 0x7F.</span><span class="sxs-lookup"><span data-stu-id="fc51e-115">It must contain characters only from the following sets: 0 through 9, A through Z, a through z, and all other punctuation except for exclamation point (\!), comma (,), opening bracket (\[), and closing bracket (\]), that is, ASCII characters 0x20, 0x22 through 0x2d, 0x2f through 0x5a, 0x5c, 0x5d through 0x7f.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc51e-116">Ele não pode começar com um espaço.</span><span class="sxs-lookup"><span data-stu-id="fc51e-116">It cannot begin with a space.</span></span>

<!-- end list -->

  - <span data-ttu-id="fc51e-117">Ele deve conter pelo menos um caractere que não seja de espaço.</span><span class="sxs-lookup"><span data-stu-id="fc51e-117">It must contain at least one non-space character.</span></span>

<span data-ttu-id="fc51e-118">**coltyp**</span><span class="sxs-lookup"><span data-stu-id="fc51e-118">**coltyp**</span></span>

<span data-ttu-id="fc51e-119">O tipo da coluna (por exemplo, texto, binário ou numérico).</span><span class="sxs-lookup"><span data-stu-id="fc51e-119">The type of the column (for example, text, binary, or numerical).</span></span> <span data-ttu-id="fc51e-120">Para obter mais informações, consulte [JET_COLTYP](./jet-coltyp.md).</span><span class="sxs-lookup"><span data-stu-id="fc51e-120">For more information, see [JET_COLTYP](./jet-coltyp.md).</span></span>

<span data-ttu-id="fc51e-121">**cbMax**</span><span class="sxs-lookup"><span data-stu-id="fc51e-121">**cbMax**</span></span>

<span data-ttu-id="fc51e-122">O comprimento máximo, em bytes, de uma coluna de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="fc51e-122">The maximum length, in bytes, of a variable-length column.</span></span> <span data-ttu-id="fc51e-123">O comprimento da coluna para colunas de comprimento fixo.</span><span class="sxs-lookup"><span data-stu-id="fc51e-123">The length of the column for fixed-length columns.</span></span>

<span data-ttu-id="fc51e-124">**grbit**</span><span class="sxs-lookup"><span data-stu-id="fc51e-124">**grbit**</span></span>

<span data-ttu-id="fc51e-125">Um grupo de bits que contém as opções para essa estrutura e que incluem zero ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="fc51e-125">A group of bits that contain the options for this structure, and which include zero or more of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fc51e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="fc51e-126">Value</span></span></p></th>
<th><p><span data-ttu-id="fc51e-127">Significado</span><span class="sxs-lookup"><span data-stu-id="fc51e-127">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-128">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="fc51e-128">JET_bitColumnFixed</span></span></p></td>
<td><p><span data-ttu-id="fc51e-129">A coluna é fixa.</span><span class="sxs-lookup"><span data-stu-id="fc51e-129">The column is fixed.</span></span> <span data-ttu-id="fc51e-130">Ele sempre usará a mesma quantidade de espaço em uma linha, independentemente da quantidade de dados que está sendo armazenada na coluna.</span><span class="sxs-lookup"><span data-stu-id="fc51e-130">It will always use the same amount of space in a row, regardless of how much data is being stored in the column.</span></span> <span data-ttu-id="fc51e-131">JET_bitColumnFixed não pode ser usada com JET_bitColumnTagged.</span><span class="sxs-lookup"><span data-stu-id="fc51e-131">JET_bitColumnFixed cannot be used with JET_bitColumnTagged.</span></span> <span data-ttu-id="fc51e-132">Esse bit não pode ser usado com valores longos, como <strong>JET_coltypLongText</strong> e <strong>JET_coltypLongBinary</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-132">This bit cannot be used with long values such as <strong>JET_coltypLongText</strong> and <strong>JET_coltypLongBinary</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-133">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="fc51e-133">JET_bitColumnTagged</span></span></p></td>
<td><p><span data-ttu-id="fc51e-134">A coluna está marcada.</span><span class="sxs-lookup"><span data-stu-id="fc51e-134">The column is tagged.</span></span> <span data-ttu-id="fc51e-135">As colunas marcadas não ocupam nenhum espaço no banco de dados se não contiverem.</span><span class="sxs-lookup"><span data-stu-id="fc51e-135">Tagged columns do not take up any space in the database if they do not contain data.</span></span> <span data-ttu-id="fc51e-136">Esse bit não pode ser usado com JET_bitColumnFixed.</span><span class="sxs-lookup"><span data-stu-id="fc51e-136">This bit cannot be used with JET_bitColumnFixed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-137">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="fc51e-137">JET_bitColumnNotNULL</span></span></p></td>
<td><p><span data-ttu-id="fc51e-138">A coluna nunca deve ser definida como um valor nulo.</span><span class="sxs-lookup"><span data-stu-id="fc51e-138">The column must never be set to a NULL value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-139">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="fc51e-139">JET_bitColumnAutoincrement</span></span></p></td>
<td><p><span data-ttu-id="fc51e-140">A coluna é incrementada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="fc51e-140">The column is automatically incremented.</span></span> <span data-ttu-id="fc51e-141">O número é um número cada vez maior e é garantido que seja exclusivo dentro de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="fc51e-141">The number is an increasing number, and is guaranteed to be unique within a table.</span></span> <span data-ttu-id="fc51e-142">No entanto, o número pode não ser contínuo.</span><span class="sxs-lookup"><span data-stu-id="fc51e-142">The number, however, might not be continuous.</span></span> <span data-ttu-id="fc51e-143">Por exemplo, se cinco linhas forem inseridas em uma tabela, a coluna AutoIncrement poderá conter os valores {1, 2, 6, 7, 8}.</span><span class="sxs-lookup"><span data-stu-id="fc51e-143">For example, if five rows are inserted into a table, the autoincrement column could contain the values { 1, 2, 6, 7, 8 }.</span></span></p>
<p><span data-ttu-id="fc51e-144"><strong>Windows 2000:  </strong> Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-144"><strong>Windows 2000:  </strong>This bit can be used only on columns of type <strong>JET_coltypLong</strong>.</span></span></p>
<p><span data-ttu-id="fc51e-145"><strong>Windows Server 2003 e posterior:  </strong> Esse bit só pode ser usado em colunas do tipo <strong>JET_coltypLong</strong> ou <strong>JET_coltypCurrency</strong>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-145"><strong>Windows Server 2003 and later:  </strong>This bit can only be used on columns of type <strong>JET_coltypLong</strong> or <strong>JET_coltypCurrency</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-146">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="fc51e-146">JET_bitColumnUpdatable</span></span></p></td>
<td><p><span data-ttu-id="fc51e-147">Esse bit é válido somente em chamadas para <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-147">This bit is valid only on calls to <a href="gg269215(v=exchg.10).md">JetGetColumnInfo</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-148">JET_bitColumnTTKey</span><span class="sxs-lookup"><span data-stu-id="fc51e-148">JET_bitColumnTTKey</span></span></p></td>
<td><p><span data-ttu-id="fc51e-149">Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-149">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-150">JET_bitColumnTTDescending</span><span class="sxs-lookup"><span data-stu-id="fc51e-150">JET_bitColumnTTDescending</span></span></p></td>
<td><p><span data-ttu-id="fc51e-151">Esse bit é válido somente em chamadas para <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-151">This bit is valid only on calls to <a href="gg269211(v=exchg.10).md">JetOpenTempTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-152">JET_bitColumnMultiValued</span><span class="sxs-lookup"><span data-stu-id="fc51e-152">JET_bitColumnMultiValued</span></span></p></td>
<td><p><span data-ttu-id="fc51e-153">A coluna pode ter valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="fc51e-153">The column can be multi-valued.</span></span> <span data-ttu-id="fc51e-154">Uma coluna com valores múltiplos pode ter zero, um ou mais valores associados a ela.</span><span class="sxs-lookup"><span data-stu-id="fc51e-154">A multi-valued column can have zero, one, or more values associated with it.</span></span> <span data-ttu-id="fc51e-155">Os vários valores em uma coluna com valores múltiplos são identificados pelo membro <strong>itagSequence</strong> de várias estruturas, por exemplo, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a> <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-155">The various values in a multi-valued column are identified by the <strong>itagSequence</strong> member of various structures, for example, <a href="gg294049(v=exchg.10).md">JET_RETINFO</a>, <a href="gg294090(v=exchg.10).md">JET_SETINFO</a>, <a href="gg269233(v=exchg.10).md">JET_SETCOLUMN</a>, <a href="gg269334(v=exchg.10).md">JET_RETRIEVECOLUMN</a>, <a href="gg294052(v=exchg.10).md">JET_ENUMCOLUMNVALUE</a>.</span></span> <span data-ttu-id="fc51e-156">Colunas com valores múltiplos devem ser colunas marcadas; ou seja, eles não podem ter colunas de comprimento fixo ou de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="fc51e-156">Multi-valued columns must be tagged columns; that is, they cannot be fixed-length or variable-length columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-157">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="fc51e-157">JET_bitColumnEscrowUpdate</span></span></p></td>
<td><p><span data-ttu-id="fc51e-158">A coluna é uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="fc51e-158">The column is an escrow update column.</span></span> <span data-ttu-id="fc51e-159">Uma coluna de atualização de caução pode ser atualizada simultaneamente por sessões diferentes com <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> e manter a consistência transacional.</span><span class="sxs-lookup"><span data-stu-id="fc51e-159">An escrow update column can be updated concurrently by different sessions with <a href="gg294125(v=exchg.10).md">JetEscrowUpdate</a> and maintain transactional consistency.</span></span></p>
<ul>
<li><p><span data-ttu-id="fc51e-160">Uma coluna de atualização de caução só pode ser criada quando a tabela está vazia.</span><span class="sxs-lookup"><span data-stu-id="fc51e-160">An escrow update column can be created only when the table is empty.</span></span></p></li>
<li><p><span data-ttu-id="fc51e-161">Uma coluna de atualização de caução deve ser do tipo <strong>JET_coltypLong.</strong></span><span class="sxs-lookup"><span data-stu-id="fc51e-161">An escrow update column must be of type <strong>JET_coltypLong.</strong></span></span></p></li>
<li><p><span data-ttu-id="fc51e-162">Uma coluna de atualização de caução deve ter um valor padrão (ou seja, <strong>cbDefault</strong> deve ser positivo).</span><span class="sxs-lookup"><span data-stu-id="fc51e-162">An escrow update column must have a default value (that is <strong>cbDefault</strong> must be positive).</span></span></p></li>
<li><p><span data-ttu-id="fc51e-163">JET_bitColumnEscrowUpdate não pode ser usado em conjunto com as seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="fc51e-163">JET_bitColumnEscrowUpdate cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="fc51e-164">JET_bitColumnTagged</span><span class="sxs-lookup"><span data-stu-id="fc51e-164">JET_bitColumnTagged</span></span></p></li>
<li><p><span data-ttu-id="fc51e-165">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="fc51e-165">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="fc51e-166">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="fc51e-166">JET_bitColumnAutoincrement</span></span></p></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-167">JET_bitColumnUnversioned</span><span class="sxs-lookup"><span data-stu-id="fc51e-167">JET_bitColumnUnversioned</span></span></p></td>
<td><p><span data-ttu-id="fc51e-168">A coluna é criada sem uma versão.</span><span class="sxs-lookup"><span data-stu-id="fc51e-168">The column is created without a version.</span></span> <span data-ttu-id="fc51e-169">Outras transações que tentarem adicionar uma coluna com o mesmo nome falharão.</span><span class="sxs-lookup"><span data-stu-id="fc51e-169">Other transactions attempting to add a column with the same name will fail.</span></span> <span data-ttu-id="fc51e-170">Esse bit só é útil com <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-170">This bit is only useful with <a href="gg294122(v=exchg.10).md">JetAddColumn</a>.</span></span> <span data-ttu-id="fc51e-171">Ele não pode ser usado em uma transação.</span><span class="sxs-lookup"><span data-stu-id="fc51e-171">It cannot be used within a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-172">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="fc51e-172">JET_bitColumnMaybeNull</span></span></p></td>
<td><p><span data-ttu-id="fc51e-173">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="fc51e-173">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-174">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="fc51e-174">JET_bitColumnFinalize</span></span></p></td>
<td><p><span data-ttu-id="fc51e-175">Use JET_bitColumnDeleteOnZero em vez de JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="fc51e-175">Use JET_bitColumnDeleteOnZero instead of JET_bitColumnFinalize.</span></span> <span data-ttu-id="fc51e-176">JET_bitColumnFinalize especifica que uma coluna pode ser finalizada.</span><span class="sxs-lookup"><span data-stu-id="fc51e-176">JET_bitColumnFinalize specifies that a column can be finalized.</span></span> <span data-ttu-id="fc51e-177">Quando uma coluna que pode ser finalizada tem uma coluna de atualização de caução que chega a zero, a linha será excluída.</span><span class="sxs-lookup"><span data-stu-id="fc51e-177">When a column that can be finalized has an escrow update column that reaches zero, the row will be deleted.</span></span> <span data-ttu-id="fc51e-178">As versões futuras podem invocar uma função de retorno de chamada em vez disso.</span><span class="sxs-lookup"><span data-stu-id="fc51e-178">Future versions can invoke a callback function instead.</span></span> <span data-ttu-id="fc51e-179">Para obter mais informações, consulte <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-179">For more information, see <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="fc51e-180">Uma coluna que pode ser finalizada deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="fc51e-180">A column that can be finalized must be an escrow update column.</span></span> <span data-ttu-id="fc51e-181">JET_bitColumnFinalize não pode ser usada com JET_bitColumnUserDefinedDefault.</span><span class="sxs-lookup"><span data-stu-id="fc51e-181">JET_bitColumnFinalize cannot be used with JET_bitColumnUserDefinedDefault.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-182">JET_bitColumnUserDefinedDefault</span><span class="sxs-lookup"><span data-stu-id="fc51e-182">JET_bitColumnUserDefinedDefault</span></span></p></td>
<td><p><span data-ttu-id="fc51e-183">O valor padrão de uma coluna é fornecido pela função de retorno de chamada, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span><span class="sxs-lookup"><span data-stu-id="fc51e-183">The default value for a column is provided by the callback function, <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>.</span></span> <span data-ttu-id="fc51e-184">Uma coluna que tem um padrão definido pelo usuário deve ser uma coluna marcada.</span><span class="sxs-lookup"><span data-stu-id="fc51e-184">A column that has a user-defined default must be a tagged column.</span></span> <span data-ttu-id="fc51e-185"><strong>pvDefault</strong> deve apontar para uma estrutura de <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> e <strong>cbDefault</strong> deve ser definido como sizeof (<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span><span class="sxs-lookup"><span data-stu-id="fc51e-185"><strong>pvDefault</strong> must point to a <a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a> structure, and <strong>cbDefault</strong> must be set to sizeof(<a href="gg269200(v=exchg.10).md">JET_USERDEFINEDDEFAULT</a>).</span></span></p>
<p><span data-ttu-id="fc51e-186">JET_bitColumnUserDefinedDefault não pode ser usado em conjunto com as seguintes constantes:</span><span class="sxs-lookup"><span data-stu-id="fc51e-186">JET_bitColumnUserDefinedDefault cannot be used in conjunction with the following constants:</span></span></p>
<ul>
<li><p><span data-ttu-id="fc51e-187">JET_bitColumnFixed</span><span class="sxs-lookup"><span data-stu-id="fc51e-187">JET_bitColumnFixed</span></span></p></li>
<li><p><span data-ttu-id="fc51e-188">JET_bitColumnNotNULL</span><span class="sxs-lookup"><span data-stu-id="fc51e-188">JET_bitColumnNotNULL</span></span></p></li>
<li><p><span data-ttu-id="fc51e-189">JET_bitColumnVersion</span><span class="sxs-lookup"><span data-stu-id="fc51e-189">JET_bitColumnVersion</span></span></p></li>
<li><p><span data-ttu-id="fc51e-190">JET_bitColumnAutoincrement</span><span class="sxs-lookup"><span data-stu-id="fc51e-190">JET_bitColumnAutoincrement</span></span></p></li>
<li><p><span data-ttu-id="fc51e-191">JET_bitColumnUpdatable</span><span class="sxs-lookup"><span data-stu-id="fc51e-191">JET_bitColumnUpdatable</span></span></p></li>
<li><p><span data-ttu-id="fc51e-192">JET_bitColumnEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="fc51e-192">JET_bitColumnEscrowUpdate</span></span></p></li>
<li><p><span data-ttu-id="fc51e-193">JET_bitColumnFinalize</span><span class="sxs-lookup"><span data-stu-id="fc51e-193">JET_bitColumnFinalize</span></span></p></li>
<li><p><span data-ttu-id="fc51e-194">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="fc51e-194">JET_bitColumnDeleteOnZero</span></span></p></li>
<li><p><span data-ttu-id="fc51e-195">JET_bitColumnMaybeNull</span><span class="sxs-lookup"><span data-stu-id="fc51e-195">JET_bitColumnMaybeNull</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-196">JET_bitColumnDeleteOnZero</span><span class="sxs-lookup"><span data-stu-id="fc51e-196">JET_bitColumnDeleteOnZero</span></span></p></td>
<td><p><span data-ttu-id="fc51e-197">A coluna é uma coluna de atualização de caução e, quando chega a zero, o registro será excluído.</span><span class="sxs-lookup"><span data-stu-id="fc51e-197">The column is an escrow update column, and when it reaches zero, the record will be deleted.</span></span> <span data-ttu-id="fc51e-198">Um uso comum para uma coluna que pode ser finalizada é usá-lo como um campo de contagem de referência e, quando o campo atinge zero, o registro é excluído.</span><span class="sxs-lookup"><span data-stu-id="fc51e-198">A common use for a column that can be finalized is to use it as a reference count field, and when the field reaches zero the record gets deleted.</span></span> <span data-ttu-id="fc51e-199">JET_bitColumnDeleteOnZero está relacionado a JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="fc51e-199">JET_bitColumnDeleteOnZero is related to JET_bitColumnFinalize.</span></span> <span data-ttu-id="fc51e-200">Uma coluna Delete-on-zero deve ser uma coluna de atualização de caução.</span><span class="sxs-lookup"><span data-stu-id="fc51e-200">A delete-on-zero column must be an escrow update column.</span></span> <span data-ttu-id="fc51e-201">JET_bitColumnDeleteOnZero não pode ser usada com JET_bitColumnFinalize.</span><span class="sxs-lookup"><span data-stu-id="fc51e-201">JET_bitColumnDeleteOnZero cannot be used with JET_bitColumnFinalize.</span></span> <span data-ttu-id="fc51e-202">JET_bitColumnDeleteOnZero não pode ser usado com colunas padrão definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="fc51e-202">JET_bitColumnDeleteOnZero cannot be used with user defined default columns.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="fc51e-203">**pvDefault**</span><span class="sxs-lookup"><span data-stu-id="fc51e-203">**pvDefault**</span></span>

<span data-ttu-id="fc51e-204">Aponta para um buffer que será o valor padrão para uma coluna.</span><span class="sxs-lookup"><span data-stu-id="fc51e-204">Points to a buffer which will be the default value for a column.</span></span> <span data-ttu-id="fc51e-205">O comprimento do buffer é **cbDefault**.</span><span class="sxs-lookup"><span data-stu-id="fc51e-205">The length of the buffer is **cbDefault**.</span></span> <span data-ttu-id="fc51e-206">Se não houver nenhum padrão, **pvDefault** deverá ser definido como NULL e **cbDefault** deverá ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="fc51e-206">If there is no default, **pvDefault** should be set to NULL and **cbDefault** should be set to zero.</span></span> <span data-ttu-id="fc51e-207">Se *grbit* tiver JET_bitColumnUserDefinedDefault definido, **pvDefault** será interpretado como um ponteiro para uma estrutura de JET_USERDEFINEDDEFAULT.</span><span class="sxs-lookup"><span data-stu-id="fc51e-207">If *grbit* has JET_bitColumnUserDefinedDefault set, **pvDefault** will be interpreted as a pointer to a JET_USERDEFINEDDEFAULT structure.</span></span> <span data-ttu-id="fc51e-208">Os valores padrão não podem ser maiores que 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="fc51e-208">Default values cannot be larger than 255 bytes.</span></span> <span data-ttu-id="fc51e-209">Se um valor padrão for maior que 255 bytes, ele será silenciosamente truncado.</span><span class="sxs-lookup"><span data-stu-id="fc51e-209">If a default value is larger than 255 bytes, it will be silently truncated.</span></span>

<span data-ttu-id="fc51e-210">**cbDefault**</span><span class="sxs-lookup"><span data-stu-id="fc51e-210">**cbDefault**</span></span>

<span data-ttu-id="fc51e-211">O tamanho, em bytes, do buffer especificado por **pvDefault**.</span><span class="sxs-lookup"><span data-stu-id="fc51e-211">The size, in bytes, of the buffer specified by **pvDefault**.</span></span>

<span data-ttu-id="fc51e-212">**cp**</span><span class="sxs-lookup"><span data-stu-id="fc51e-212">**cp**</span></span>

<span data-ttu-id="fc51e-213">A página de código da coluna.</span><span class="sxs-lookup"><span data-stu-id="fc51e-213">The code page for the column.</span></span> <span data-ttu-id="fc51e-214">Os únicos valores válidos para colunas de texto são Inglês (1252) e Unicode (1200).</span><span class="sxs-lookup"><span data-stu-id="fc51e-214">The only valid values for text columns are English (1252) and Unicode (1200).</span></span> <span data-ttu-id="fc51e-215">Um valor de zero significa que o padrão será usado (Inglês, 1252).</span><span class="sxs-lookup"><span data-stu-id="fc51e-215">A value of zero means the default will be used (English, 1252).</span></span> <span data-ttu-id="fc51e-216">Se a coluna não for uma coluna de texto, a página de código será definida automaticamente como zero.</span><span class="sxs-lookup"><span data-stu-id="fc51e-216">If the column is not a text column, the code page automatically gets set to zero.</span></span>

<span data-ttu-id="fc51e-217">**columnid**</span><span class="sxs-lookup"><span data-stu-id="fc51e-217">**columnid**</span></span>

<span data-ttu-id="fc51e-218">Em caso de sucesso, o identificador de coluna da coluna recém-criada será passado de volta neste campo.</span><span class="sxs-lookup"><span data-stu-id="fc51e-218">On success, the column identifier of the newly-created column will be passed back in this field.</span></span> <span data-ttu-id="fc51e-219">Em caso de falha, o valor é indefinido.</span><span class="sxs-lookup"><span data-stu-id="fc51e-219">On failure, the value is undefined.</span></span>

<span data-ttu-id="fc51e-220">**erra**</span><span class="sxs-lookup"><span data-stu-id="fc51e-220">**err**</span></span>

<span data-ttu-id="fc51e-221">O campo **Err** conterá o status da criação desta coluna.</span><span class="sxs-lookup"><span data-stu-id="fc51e-221">The **err** field will contain the status of creating this column.</span></span> <span data-ttu-id="fc51e-222">Consulte [JetAddColumn](./jetaddcolumn-function.md) para obter uma lista de valores de retorno prováveis.</span><span class="sxs-lookup"><span data-stu-id="fc51e-222">See [JetAddColumn](./jetaddcolumn-function.md) for a list of likely return values.</span></span>

### <a name="requirements"></a><span data-ttu-id="fc51e-223">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc51e-223">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-224"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="fc51e-224"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="fc51e-225">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="fc51e-225">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-226"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="fc51e-226"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="fc51e-227">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="fc51e-227">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc51e-228"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="fc51e-228"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="fc51e-229">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="fc51e-229">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc51e-230"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="fc51e-230"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="fc51e-231">Implementado como <strong>JET_COLUMNCREATE_W</strong> (Unicode) e <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="fc51e-231">Implemented as <strong>JET_COLUMNCREATE_W</strong> (Unicode) and <strong>JET_COLUMNCREATE_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="fc51e-232">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="fc51e-232">See Also</span></span>

[<span data-ttu-id="fc51e-233">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="fc51e-233">JET_COLTYP</span></span>](./jet-coltyp.md)  
[<span data-ttu-id="fc51e-234">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="fc51e-234">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="fc51e-235">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="fc51e-235">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="fc51e-236">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="fc51e-236">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="fc51e-237">JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="fc51e-237">JET_RETINFO</span></span>](./jet-retinfo-structure.md)  
[<span data-ttu-id="fc51e-238">JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="fc51e-238">JET_SETINFO</span></span>](./jet-setinfo-structure.md)  
[<span data-ttu-id="fc51e-239">JET_SETCOLUMN</span><span class="sxs-lookup"><span data-stu-id="fc51e-239">JET_SETCOLUMN</span></span>](./jet-setcolumn-structure.md)  
[<span data-ttu-id="fc51e-240">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="fc51e-240">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="fc51e-241">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="fc51e-241">JET_ENUMCOLUMNVALUE</span></span>](./jet-enumcolumnvalue-structure.md)  
[<span data-ttu-id="fc51e-242">JetAddColumn</span><span class="sxs-lookup"><span data-stu-id="fc51e-242">JetAddColumn</span></span>](./jetaddcolumn-function.md)  
[<span data-ttu-id="fc51e-243">JetCreateTableColumnIndex</span><span class="sxs-lookup"><span data-stu-id="fc51e-243">JetCreateTableColumnIndex</span></span>](./jetcreatetablecolumnindex-function.md)  
[<span data-ttu-id="fc51e-244">JetCreateTableColumnIndex2</span><span class="sxs-lookup"><span data-stu-id="fc51e-244">JetCreateTableColumnIndex2</span></span>](./jetcreatetablecolumnindex2-function.md)  
[<span data-ttu-id="fc51e-245">JetEscrowUpdate</span><span class="sxs-lookup"><span data-stu-id="fc51e-245">JetEscrowUpdate</span></span>](./jetescrowupdate-function.md)  
[<span data-ttu-id="fc51e-246">JetRenameColumn</span><span class="sxs-lookup"><span data-stu-id="fc51e-246">JetRenameColumn</span></span>](./jetrenamecolumn-function.md)  
[<span data-ttu-id="fc51e-247">JetSetColumns</span><span class="sxs-lookup"><span data-stu-id="fc51e-247">JetSetColumns</span></span>](./jetsetcolumns-function.md)
