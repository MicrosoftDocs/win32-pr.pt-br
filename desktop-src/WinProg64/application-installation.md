---
title: Instalação de aplicativos em sistemas de 64 bits
description: o Windows Installer de 64 bits pode instalar diretamente aplicativos baseados em MSI de 32 bits em Windows de 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalação do aplicativo 64-bit Windows programação
- instalação do 64-bit Windows Programming
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643596"
---
# <a name="application-installation-on-64-bit-systems"></a>Instalação de aplicativos em sistemas de 64 bits

o [Windows Installer de 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) pode instalar diretamente aplicativos baseados em MSI de 32 bits em Windows de 64 bits. para aplicativos mais antigos que usam um stub de 16 bits para iniciar um mecanismo de instalação de 32 bits, 64 bits Windows reconhece programas de instalador de 16 bits específicos e substitui uma versão de 32 bits portada.

os aplicativos DOS de 16 bits, Windows ou so/2 geralmente usam um stub de 16 bits para verificar o tipo de computador e, em seguida, iniciar um mecanismo de instalação de 32 bits para realmente executar a instalação. para habilitar a instalação de aplicativos que usam essa técnica, o 64-bit Windows substitui as versões de 32 bits pelos seguintes programas de instalação de 16 bits:

* instalação da Microsoft para Windows 1,2  
* instalação da Microsoft para Windows 2,6  
* instalação da Microsoft para Windows 3,0  
* instalação da Microsoft para Windows 3, 1  
* InstallShield 5. x  

a lista de substituições é armazenada no registro na seguinte chave: **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Esse mecanismo é fornecido apenas para compatibilidade com aplicativos de 32 bits que usam os programas do Microsoft Installer de 16 bits listados neste tópico. Não há suporte para a adição de programas de instalador de terceiros.

 

> [!Note]  
> esse mecanismo não está incluído em Windows 10 no ARM.

 

 

 