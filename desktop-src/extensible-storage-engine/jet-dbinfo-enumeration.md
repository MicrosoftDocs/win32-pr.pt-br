---
description: 'Saiba mais sobre: enumeração de JET_DbInfo'
title: Enumeração de JET_DbInfo
TOCTitle: JET_DbInfo enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DbInfo
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfo(v=EXCHG.10)
ms:contentKeyID: 39516181
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DbInfo.DBInUse
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filename
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Filesize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.FileType
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceOwned
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Misc
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Options
- Microsoft.Isam.Esent.Interop.JET_DbInfo.PageSize
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Transactions
- Microsoft.Isam.Esent.Interop.JET_DbInfo
- Microsoft.Isam.Esent.Interop.JET_DbInfo.LCID
- Microsoft.Isam.Esent.Interop.JET_DbInfo.Version
- Microsoft.Isam.Esent.Interop.JET_DbInfo.SpaceAvailable
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 39c6c3175c08e4f7644ad4f0b41137e12e84f71d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771268"
---
# <a name="jet_dbinfo-enumeration"></a><span data-ttu-id="2ca83-103">Enumeração de JET_DbInfo</span><span class="sxs-lookup"><span data-stu-id="2ca83-103">JET_DbInfo enumeration</span></span>

<span data-ttu-id="2ca83-104">Níveis de informações para recuperar informações do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="2ca83-104">Info levels for retrieving database info.</span></span>

<span data-ttu-id="2ca83-105">**Namespace:**  [Microsoft. ISAM. ESENT. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2ca83-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2ca83-106">**Assembly:**  Microsoft. ISAM. ESENT. Interop (em Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="2ca83-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2ca83-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ca83-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_DbInfo
'Usage
Dim instance As JET_DbInfo
```

``` csharp
public enum JET_DbInfo
```

## <a name="members"></a><span data-ttu-id="2ca83-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2ca83-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="2ca83-109">Nome do membro</span><span class="sxs-lookup"><span data-stu-id="2ca83-109">Member name</span></span></th>
<th><span data-ttu-id="2ca83-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="2ca83-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-111">Nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="2ca83-111">Filename</span></span></td>
<td><span data-ttu-id="2ca83-112">Retorna o caminho para o arquivo de banco de dados (cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="2ca83-112">Returns the path to the database file (string).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-113">LCID</span><span class="sxs-lookup"><span data-stu-id="2ca83-113">LCID</span></span></td>
<td><span data-ttu-id="2ca83-114">Retorna o LCID (identificador de localidade) associado a este banco de dados (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-114">Returns the locale identifier (LCID) associated with this database (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-115">Opções</span><span class="sxs-lookup"><span data-stu-id="2ca83-115">Options</span></span></td>
<td><span data-ttu-id="2ca83-116">Retorna um <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span><span class="sxs-lookup"><span data-stu-id="2ca83-116">Returns a <a href="hh579532(v=exchg.10).md">OpenDatabaseGrbit</a>.</span></span> <span data-ttu-id="2ca83-117">Isso indica se o banco de dados está aberto em modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2ca83-117">This indicates whether the database is opened in exclusive mode.</span></span> <span data-ttu-id="2ca83-118">Se o banco de dados estiver em modo exclusivo, o <a href="hh579532(v=exchg.10).md">exclusivo</a> será retornado, caso contrário, zero será retornado.</span><span class="sxs-lookup"><span data-stu-id="2ca83-118">If the database is in exclusive mode then <a href="hh579532(v=exchg.10).md">Exclusive</a> will be returned, otherwise zero is returned.</span></span> <span data-ttu-id="2ca83-119">Outras opções de grbit de banco de dados para JetAttachDatabase e JetOpenDatabase não são retornadas.</span><span class="sxs-lookup"><span data-stu-id="2ca83-119">Other database grbit options for JetAttachDatabase and JetOpenDatabase are not returned.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-120">Transactions</span><span class="sxs-lookup"><span data-stu-id="2ca83-120">Transactions</span></span></td>
<td><span data-ttu-id="2ca83-121">Retorna um número um maior do que o nível máximo para o qual as transações podem ser aninhadas.</span><span class="sxs-lookup"><span data-stu-id="2ca83-121">Returns a number one greater than the maximum level to which transactions can be nested.</span></span> <span data-ttu-id="2ca83-122">Se <a href="dn292105(v=exchg.10).md">JetBeginTransaction (JET_SESID)</a> for chamado (em um modo de aninhamento, ou seja, na mesma sessão, sem uma confirmação ou reversão) quantas vezes esse valor, na última chamada, <a href="hh564840(v=exchg.10).md">TransTooDeep</a> será retornado (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-122">If <a href="dn292105(v=exchg.10).md">JetBeginTransaction(JET_SESID)</a> is called (in a nesting fashion, that is, on the same session, without a commit or rollback) as many times as this value, on the last call <a href="hh564840(v=exchg.10).md">TransTooDeep</a> will be returned (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-123">Versão</span><span class="sxs-lookup"><span data-stu-id="2ca83-123">Version</span></span></td>
<td><span data-ttu-id="2ca83-124">Retorna a versão principal do mecanismo de banco de dados (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-124">Returns the major version of the database engine (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-125">Tamanho</span><span class="sxs-lookup"><span data-stu-id="2ca83-125">Filesize</span></span></td>
<td><span data-ttu-id="2ca83-126">Retorna o tamanho do banco de dados, em páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-126">Returns the filesize of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-127">SpaceOwned</span><span class="sxs-lookup"><span data-stu-id="2ca83-127">SpaceOwned</span></span></td>
<td><span data-ttu-id="2ca83-128">Retorna o espaço de Propriedade do banco de dados, em páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-128">Returns the owned space of the database, in pages (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-129">SpaceAvailable</span><span class="sxs-lookup"><span data-stu-id="2ca83-129">SpaceAvailable</span></span></td>
<td><span data-ttu-id="2ca83-130">Retorna o espaço disponível no banco de dados, em páginas (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-130">Returns the available space in the database, in pages (Int32).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-131">Diversos</span><span class="sxs-lookup"><span data-stu-id="2ca83-131">Misc</span></span></td>
<td><span data-ttu-id="2ca83-132">Retorna um objeto <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> .</span><span class="sxs-lookup"><span data-stu-id="2ca83-132">Returns a <a href="hh538867(v=exchg.10).md">JET_DBINFOMISC</a> object.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-133">DBInUse</span><span class="sxs-lookup"><span data-stu-id="2ca83-133">DBInUse</span></span></td>
<td><span data-ttu-id="2ca83-134">Retorna um valor booleano que indica se o banco de dados está anexado (booliano).</span><span class="sxs-lookup"><span data-stu-id="2ca83-134">Returns a boolean indicating whether the database is attached (boolean).</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="2ca83-135">PageSize</span><span class="sxs-lookup"><span data-stu-id="2ca83-135">PageSize</span></span></td>
<td><span data-ttu-id="2ca83-136">Retorna o tamanho da página do banco de dados (Int32).</span><span class="sxs-lookup"><span data-stu-id="2ca83-136">Returns the page size of the database (Int32).</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="2ca83-137">FileType</span><span class="sxs-lookup"><span data-stu-id="2ca83-137">FileType</span></span></td>
<td><span data-ttu-id="2ca83-138">Retorna o tipo do banco de dados (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span><span class="sxs-lookup"><span data-stu-id="2ca83-138">Returns the type of the database (<a href="hh566739(v=exchg.10).md">JET_filetype</a>).</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="2ca83-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ca83-139">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ca83-140">Referência</span><span class="sxs-lookup"><span data-stu-id="2ca83-140">Reference</span></span>

[<span data-ttu-id="2ca83-141">Namespace Microsoft. ISAM. ESENT. Interop</span><span class="sxs-lookup"><span data-stu-id="2ca83-141">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
