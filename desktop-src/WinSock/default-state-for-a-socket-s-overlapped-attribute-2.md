---
description: A função socket criou soquetes com o atributo Overlapped definido por padrão na primeira Wsock32.dll, a versão de 32 bits do Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Estado padrão para o atributo sobreposto de um soquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090398"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a>Estado padrão para o atributo sobreposto de um soquete

A função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) criou soquetes com o atributo Overlapped definido por padrão na primeira Wsock32.dll, a versão de 32 bits do Windows sockets 1,1. Para garantir a compatibilidade com versões anteriores atualmente implantadas Wsock32.dll, isso continuará sendo o caso do Windows Sockets 2 também. Ou seja, nos soquetes do Windows Sockets 2 criados com a função **Socket** terão o atributo Overlapped. No entanto, para ser mais compatível com o restante da API do Windows, os soquetes criados com [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) não serão, por padrão, o atributo sobreposto. Esse atributo só será aplicado se o \_ bit sobreposto do sinalizador WSA \_ estiver definido.

 

 



