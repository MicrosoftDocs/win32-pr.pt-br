---
description: Um aplicativo que usa uma autoridade de backup para armazenar chaves de sessão geralmente segue estas etapas.
ms.assetid: 859310ed-6000-44c8-92f7-974326ce0fc9
title: Armazenando chaves de sessão usando uma autoridade de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59906874f384d4eed9e20d6a781b14e3feba313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296794"
---
# <a name="storing-session-keys-using-a-backup-authority"></a><span data-ttu-id="a5261-103">Armazenando chaves de sessão usando uma autoridade de backup</span><span class="sxs-lookup"><span data-stu-id="a5261-103">Storing Session Keys Using a Backup Authority</span></span>

<span data-ttu-id="a5261-104">Um aplicativo que usa uma [*autoridade de backup*](../secgloss/b-gly.md) para armazenar chaves de sessão geralmente segue estas etapas.</span><span class="sxs-lookup"><span data-stu-id="a5261-104">An application using a [*backup authority*](../secgloss/b-gly.md) to store session keys typically follows these steps.</span></span>

<span data-ttu-id="a5261-105">**Para usar uma autoridade de backup**</span><span class="sxs-lookup"><span data-stu-id="a5261-105">**To use a backup authority**</span></span>

1.  <span data-ttu-id="a5261-106">Criptografe o arquivo como de costume.</span><span class="sxs-lookup"><span data-stu-id="a5261-106">Encrypt the file as usual.</span></span>
2.  <span data-ttu-id="a5261-107">Exporte a [*chave de sessão*](../secgloss/s-gly.md) usada para criptografar o arquivo em um blob de [*chave simples*](../secgloss/s-gly.md), especificando que sua própria [*chave pública de troca de chave*](../secgloss/k-gly.md) seja usada para criptografar o blob de chave.</span><span class="sxs-lookup"><span data-stu-id="a5261-107">Export the [*session key*](../secgloss/s-gly.md) used to encrypt the file into a [*simple key BLOB*](../secgloss/s-gly.md), specifying that your own [*key exchange public key*](../secgloss/k-gly.md) be used to encrypt the key BLOB.</span></span> <span data-ttu-id="a5261-108">Armazene esse BLOB de chave com o arquivo criptografado.</span><span class="sxs-lookup"><span data-stu-id="a5261-108">Store this key BLOB with the encrypted file.</span></span>
3.  <span data-ttu-id="a5261-109">Exporte a chave de sessão novamente, desta vez especificando que a chave pública da autoridade de backup seja usada para criptografar o BLOB de chave.</span><span class="sxs-lookup"><span data-stu-id="a5261-109">Export the session key again, this time specifying that the backup authority's public key be used to encrypt the key BLOB.</span></span> <span data-ttu-id="a5261-110">Envie esse BLOB de chave para a autoridade de backup, junto com a descrição da chave, o número de série e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a5261-110">Send this key BLOB to the backup authority, along with the key's description, serial number, and so on.</span></span>

<span data-ttu-id="a5261-111">Se um [*par de chaves*](../secgloss/k-gly.md) for perdido, as chaves poderão ser recuperadas da [*autoridade de backup*](../secgloss/b-gly.md) se a identidade do proprietário das chaves puder ser estabelecida.</span><span class="sxs-lookup"><span data-stu-id="a5261-111">If a [*key pair*](../secgloss/k-gly.md) is lost, the keys can be retrieved from the [*backup authority*](../secgloss/b-gly.md) if the identity of the keys' owner can be established.</span></span> <span data-ttu-id="a5261-112">O procedimento para estabelecer a identidade é determinado pela política da autoridade de backup específica e não envolve o CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="a5261-112">The procedure for establishing identity is determined by the policy of the particular backup authority and does not involve CryptoAPI.</span></span>

<span data-ttu-id="a5261-113">Para o código necessário para criar uma chave de sessão e exportar essa chave para um [*blob de chave simples*](../secgloss/s-gly.md) que pode ser gravado em um arquivo de disco, consulte [o programa de exemplo C: exportando uma chave de sessão](example-c-program-exporting-a-session-key.md).</span><span class="sxs-lookup"><span data-stu-id="a5261-113">For the code needed to create a session key and export that key to a [*simple key BLOB*](../secgloss/s-gly.md) that can be written to a disk file, see [Example C Program: Exporting a Session Key](example-c-program-exporting-a-session-key.md).</span></span>

 

 
