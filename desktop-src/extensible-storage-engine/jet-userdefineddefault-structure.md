---
description: 'Saiba mais sobre: estrutura de JET_USERDEFINEDDEFAULT'
title: Estrutura de JET_USERDEFINEDDEFAULT
TOCTitle: JET_USERDEFINEDDEFAULT Structure
ms:assetid: 1f0a5419-9fae-4a93-a271-2f9772ecc996
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269200(v=EXCHG.10)
ms:contentKeyID: 32765503
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
ms.openlocfilehash: e5f588588a1a6769e997264321f8911a86e169c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811507"
---
# <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="bd06c-103">Estrutura de JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bd06c-103">JET_USERDEFINEDDEFAULT Structure</span></span>


<span data-ttu-id="bd06c-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bd06c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_userdefineddefault-structure"></a><span data-ttu-id="bd06c-105">Estrutura de JET_USERDEFINEDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bd06c-105">JET_USERDEFINEDDEFAULT Structure</span></span>

<span data-ttu-id="bd06c-106">A estrutura de **JET_USERDEFINEDDEFAULT** é especificada em conjunto com JET_bitColumnUserDefinedDefault para dar uma nova coluna um valor padrão que é determinado usando um retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bd06c-106">The **JET_USERDEFINEDDEFAULT** structure is specified in conjunction with JET_bitColumnUserDefinedDefault to give a new column a default value that is determined using a callback.</span></span> <span data-ttu-id="bd06c-107">Essa técnica pode ser usada para implementar colunas computadas.</span><span class="sxs-lookup"><span data-stu-id="bd06c-107">This technique can be used to implement computed columns.</span></span>

<span data-ttu-id="bd06c-108">**Windows XP:** A estrutura de **JET_USERDEFINEDDEFAULT** é introduzida no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bd06c-108">**Windows XP:** The **JET_USERDEFINEDDEFAULT** structure is introduced in Windows XP.</span></span>

```cpp
    typedef struct tag_JET_USERDEFINEDDEFAULT {
      tchar* szCallback;
      unsigned char* pbUserData;
      unsigned long cbUserData;
      tchar* szDependantColumns;
    } JET_USERDEFINEDDEFAULT;
```

### <a name="members"></a><span data-ttu-id="bd06c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="bd06c-109">Members</span></span>

<span data-ttu-id="bd06c-110">**szCallback**</span><span class="sxs-lookup"><span data-stu-id="bd06c-110">**szCallback**</span></span>

<span data-ttu-id="bd06c-111">O nome de exportação da função que implementa o retorno de chamada no \! formato "função de módulo".</span><span class="sxs-lookup"><span data-stu-id="bd06c-111">The export name of the function that implements the callback in "module\!function" format.</span></span>

<span data-ttu-id="bd06c-112">O retorno de chamada persiste como parte do esquema de coluna.</span><span class="sxs-lookup"><span data-stu-id="bd06c-112">The callback persists as a part of the column schema.</span></span> <span data-ttu-id="bd06c-113">O executável real do host e o nome de exportação da função devem persistir para habilitar a pesquisa do endereço verdadeiro da função em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="bd06c-113">The actual host executable and export name of the function must persist to enable the lookup of the true address of the function at run time.</span></span>

<span data-ttu-id="bd06c-114">O nome do módulo é o nome do binário do host que contém a função.</span><span class="sxs-lookup"><span data-stu-id="bd06c-114">The module name is the name of the host binary that contains the function.</span></span> <span data-ttu-id="bd06c-115">O nome da função é o nome da exportação para essa função.</span><span class="sxs-lookup"><span data-stu-id="bd06c-115">The function name is the name of the export for that function.</span></span> <span data-ttu-id="bd06c-116">Essas duas informações serão usadas pelo mecanismo de banco de dados em tempo de execução para localizar o endereço verdadeiro do retorno de chamada, executando uma chamadas [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) no nome do módulo seguido por uma chamada de [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) no nome da função.</span><span class="sxs-lookup"><span data-stu-id="bd06c-116">These two pieces of information will be used by the database engine at runtime to locate the true address of the callback by executing a [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) call on the module name followed by a [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) call on the function name.</span></span>

<span data-ttu-id="bd06c-117">Por exemplo, se o retorno de chamada tiver sido implementado em uma DLL chamada MyCallback.DLL e essa DLL fosse armazenada em C: \\ MyApplication e a função que implementa o retorno de chamada fosse exportada da dll como UserDefinedDefaultCallback, a cadeia de caracteres necessária seria "C: \\ MyApplication \\MyCallback.DLL\! UserDefinedDefaultCallback".</span><span class="sxs-lookup"><span data-stu-id="bd06c-117">For example, if the callback were implemented in a DLL called MyCallback.DLL and that DLL were stored in C:\\MyApplication and the function implementing the callback were exported from the DLL as UserDefinedDefaultCallback, then the required string would be "C:\\MyApplication\\MyCallback.DLL\!UserDefinedDefaultCallback".</span></span>

<span data-ttu-id="bd06c-118">**Observação**  Inserido " \! "</span><span class="sxs-lookup"><span data-stu-id="bd06c-118">**Note**  Embedded "\!"</span></span> <span data-ttu-id="bd06c-119">Não há suporte para caracteres na parte do módulo do nome do retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bd06c-119">characters in the module portion of the callback name are not supported.</span></span>

<span data-ttu-id="bd06c-120">É altamente recomendável que você use um nome de retorno de chamada que não seja uma função da arquitetura do host.</span><span class="sxs-lookup"><span data-stu-id="bd06c-120">It is highly recommended that you use a callback name that is not a function of the host architecture.</span></span> <span data-ttu-id="bd06c-121">Por exemplo, não use exportações decoradas como stdcall ( UserDefinedDefaultCallback@32 ) porque essa Convenção de chamada só tem suporte em computadores x86.</span><span class="sxs-lookup"><span data-stu-id="bd06c-121">For example, do not use exports decorated as stdcall (UserDefinedDefaultCallback@32) because this calling convention is only supported on x86 machines.</span></span> <span data-ttu-id="bd06c-122">Se um retorno de chamada for usado, o banco de dados só poderá ser usado em um computador x86.</span><span class="sxs-lookup"><span data-stu-id="bd06c-122">If such a callback were used then the database could only be used on an x86 machine.</span></span> <span data-ttu-id="bd06c-123">Um alias deve ser usado para fazer uma exportação independente de plataforma nesse caso.</span><span class="sxs-lookup"><span data-stu-id="bd06c-123">An alias should be used to make a platform-agnostic export in this case.</span></span>

<span data-ttu-id="bd06c-124">É altamente recomendável que você use o caminho completo do nome do módulo que está implementando o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="bd06c-124">It is highly recommended that you use the full path of the module name that is implementing the callback.</span></span> <span data-ttu-id="bd06c-125">Se um caminho relativo for usado, o processo que está hospedando o banco de dados poderá ser suscetível a ataques por um binário não autorizado.</span><span class="sxs-lookup"><span data-stu-id="bd06c-125">If a relative path is used then the process that is hosting the database might be susceptible to attack by a rogue binary.</span></span>

<span data-ttu-id="bd06c-126">O aplicativo deve passar apenas retornos de chamada confiáveis para o mecanismo de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd06c-126">The application should pass only trusted callbacks to the database engine.</span></span> <span data-ttu-id="bd06c-127">O mecanismo de banco de dados carregará o binário para verificar sua existência quando a coluna associada for criada.</span><span class="sxs-lookup"><span data-stu-id="bd06c-127">The database engine will load the binary to verify its existence when the associated column is created.</span></span> <span data-ttu-id="bd06c-128">Se o caminho para o binário não for validado ou conhecido como confiável, ele poderá atacar o processo que está hospedando o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd06c-128">If the path to the binary is not validated or known to be trusted then it could attack the process that is hosting the database.</span></span>

<span data-ttu-id="bd06c-129">**pbUserData**</span><span class="sxs-lookup"><span data-stu-id="bd06c-129">**pbUserData**</span></span>

<span data-ttu-id="bd06c-130">Um bloco autocontido de dados definidos pelo usuário a ser passado para o retorno de chamada quando invocado. O bloco de dados fornecido continuará como parte do esquema de coluna.</span><span class="sxs-lookup"><span data-stu-id="bd06c-130">A self-contained block of user-defined data to be passed to the callback when invoked.The data block that is provided will persist as a part of the column schema.</span></span> <span data-ttu-id="bd06c-131">Como resultado, o bloco de dados deve ser totalmente independente e não pode se referir a todos os dados que estão fora do escopo do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="bd06c-131">As a result, the data block must be entirely self-contained and cannot refer to any data that is outside the scope of the database.</span></span>

<span data-ttu-id="bd06c-132">Se **pbUserData** for zero, o valor de **cbUserData** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="bd06c-132">If **pbUserData** is zero then the value of **cbUserData** is ignored.</span></span> <span data-ttu-id="bd06c-133">Nesse caso, nenhum dado definido pelo usuário será passado para o retorno de chamada quando for invocado.</span><span class="sxs-lookup"><span data-stu-id="bd06c-133">In this case, no user-defined data will be passed to the callback when invoked.</span></span>

<span data-ttu-id="bd06c-134">**cbUserData**</span><span class="sxs-lookup"><span data-stu-id="bd06c-134">**cbUserData**</span></span>

<span data-ttu-id="bd06c-135">Consulte **pbUserData**.</span><span class="sxs-lookup"><span data-stu-id="bd06c-135">See **pbUserData**.</span></span>

<span data-ttu-id="bd06c-136">**szDependantColumns**</span><span class="sxs-lookup"><span data-stu-id="bd06c-136">**szDependantColumns**</span></span>

<span data-ttu-id="bd06c-137">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="bd06c-137">Reserved for future use.</span></span>

<span data-ttu-id="bd06c-138">Esse membro sempre deve ser definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="bd06c-138">This member should always be set to NULL.</span></span>

### <a name="requirements"></a><span data-ttu-id="bd06c-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd06c-139">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd06c-140"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bd06c-140"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bd06c-141">Requer o Windows Vista, o Windows XP ou o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bd06c-141">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd06c-142"><strong>Servidor</strong></span><span class="sxs-lookup"><span data-stu-id="bd06c-142"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bd06c-143">Requer o Windows Server 2008, o Windows Server 2003 ou o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bd06c-143">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd06c-144"><strong>Cabeçalho</strong></span><span class="sxs-lookup"><span data-stu-id="bd06c-144"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bd06c-145">Declarado em ESENT. h.</span><span class="sxs-lookup"><span data-stu-id="bd06c-145">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd06c-146"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="bd06c-146"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="bd06c-147">Implementado como <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) e <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="bd06c-147">Implemented as <strong>JET_ USERDEFINEDDEFAULT_W</strong> (Unicode) and <strong>JET_ USERDEFINEDDEFAULT_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bd06c-148">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="bd06c-148">See Also</span></span>

[<span data-ttu-id="bd06c-149">JET_CBTYP</span><span class="sxs-lookup"><span data-stu-id="bd06c-149">JET_CBTYP</span></span>](./jet-cbtyp.md)  
[<span data-ttu-id="bd06c-150">JET_COLUMNCREATE</span><span class="sxs-lookup"><span data-stu-id="bd06c-150">JET_COLUMNCREATE</span></span>](./jet-columncreate-structure.md)  
[<span data-ttu-id="bd06c-151">JET_COLUMNDEF</span><span class="sxs-lookup"><span data-stu-id="bd06c-151">JET_COLUMNDEF</span></span>](./jet-columndef-structure.md)
