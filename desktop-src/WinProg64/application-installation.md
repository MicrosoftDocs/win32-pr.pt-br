---
title: Instalação de aplicativos em sistemas de 64 bits
description: O Windows Installer de 64 bits pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits.
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- instalação de aplicativo 64-programação do Windows-bit
- Programação de instalação do Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084676"
---
# <a name="application-installation-on-64-bit-systems"></a>Instalação de aplicativos em sistemas de 64 bits

O [Windows Installer de 64 bits](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) pode instalar diretamente aplicativos baseados em MSI de 32 bits em janelas de 64 bits. Para aplicativos mais antigos que usam um stub de 16 bits para iniciar um mecanismo de instalação de 32 bits, o Windows de 64 bits reconhece programas de instalador específicos de 16 bits e substitui uma versão de 32 bits portada.

aplicativos DOS de 16 bits, do Windows ou do SO/2 geralmente usam um stub de 16 bits para verificar o tipo de computador e, em seguida, iniciar um mecanismo de instalação de 32 bits para realmente executar a instalação. Para habilitar a instalação de aplicativos que usam essa técnica, o Windows de 64 bits substitui as versões de 32 bits pelos seguintes programas de instalação de 16 bits:

* Instalação da Microsoft para Windows 1,2  
* Instalação da Microsoft para Windows 2,6  
* Instalação da Microsoft para Windows 3,0  
* Instalação da Microsoft para Windows 3, 1  
* InstallShield 5. x  

A lista de substituições é armazenada no registro na seguinte chave: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**.

> [!Note]  
> Esse mecanismo é fornecido apenas para compatibilidade com aplicativos de 32 bits que usam os programas do Microsoft Installer de 16 bits listados neste tópico. Não há suporte para a adição de programas de instalador de terceiros.

 

> [!Note]  
> Esse mecanismo não está incluído no Windows 10 no ARM.

 

 

 