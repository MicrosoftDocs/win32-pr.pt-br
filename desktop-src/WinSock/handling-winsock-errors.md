---
description: Tratamento de erros no Winsock.
ms.assetid: 81ed3328-4b15-43dc-88f1-573a4a97d672
title: Manipulando erros do Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbad01ad7add7995cf978e101535104f6dc0da6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807870"
---
# <a name="handling-winsock-errors"></a><span data-ttu-id="f9a9c-103">Manipulando erros do Winsock</span><span class="sxs-lookup"><span data-stu-id="f9a9c-103">Handling Winsock Errors</span></span>

<span data-ttu-id="f9a9c-104">A maioria das funções do Windows Sockets 2 não retorna a causa específica de um erro quando a função retorna.</span><span class="sxs-lookup"><span data-stu-id="f9a9c-104">Most Windows Sockets 2 functions do not return the specific cause of an error when the function returns.</span></span> <span data-ttu-id="f9a9c-105">Algumas funções do Winsock retornarão um valor zero se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="f9a9c-105">Some Winsock functions return a value of zero if successful.</span></span> <span data-ttu-id="f9a9c-106">Caso contrário, o valor de erro de soquete \_ (-1) é retornado e um número de erro específico pode ser recuperado chamando a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f9a9c-106">Otherwise, the value SOCKET\_ERROR (-1) is returned and a specific error number can be retrieved by calling the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function.</span></span> <span data-ttu-id="f9a9c-107">Para funções do Winsock que retornam um identificador, um valor de retorno de \_ soquete inválido (0xFFFF) indica um erro e um número de erro específico pode ser recuperado chamando **WSAGetLastError**.</span><span class="sxs-lookup"><span data-stu-id="f9a9c-107">For Winsock functions that return a handle, a return value of INVALID\_SOCKET (0xffff) indicates an error and a specific error number can be retrieved by calling **WSAGetLastError**.</span></span> <span data-ttu-id="f9a9c-108">Para funções do Winsock que retornam um ponteiro, um valor de retorno de **NULL** indica um erro e um número de erro específico pode ser recuperado chamando a função **WSAGetLastError** .</span><span class="sxs-lookup"><span data-stu-id="f9a9c-108">For Winsock functions that return a pointer, a return value of **NULL** indicates an error and a specific error number can be retrieved by calling the **WSAGetLastError** function.</span></span>

<span data-ttu-id="f9a9c-109">Um código de erro do Winsock pode ser convertido em um HRESULT para uso em uma RPC (chamada de procedimento remoto) usando HRESULT \_ do \_ Win32.</span><span class="sxs-lookup"><span data-stu-id="f9a9c-109">A Winsock error code can be converted to an HRESULT for use in a remote procedure call (RPC) using HRESULT\_FROM\_WIN32.</span></span> <span data-ttu-id="f9a9c-110">Em versões anteriores do SDK (Software Development Kit) da plataforma, \_ o HRESULT do \_ Win32 foi definido como uma macro no arquivo de cabeçalho *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="f9a9c-110">In earlier versions of the Platform Software Development Kit (SDK), HRESULT\_FROM\_WIN32 was defined as a macro in the *Winerror.h* header file.</span></span> <span data-ttu-id="f9a9c-111">No SDK (Software Development Kit) do Microsoft Windows, o HRESULT \_ do \_ Win32 é definido como uma função embutida no arquivo de cabeçalho *Winerror. h* .</span><span class="sxs-lookup"><span data-stu-id="f9a9c-111">In the Microsoft Windows Software Development Kit (SDK), HRESULT\_FROM\_WIN32 is defined as an inline function in the *Winerror.h* header file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9a9c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9a9c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9a9c-113">Códigos de erro do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="f9a9c-113">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> </dl>

 

 



