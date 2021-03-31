---
title: Vinculando à DLL de acesso remoto
description: Se um aplicativo for vinculado estaticamente à DLL RASAPI32, o aplicativo não será carregado se o serviço de acesso remoto não estiver instalado.
ms.assetid: a2399406-f73c-40aa-877c-80f2f99ed10a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dd8b29eab4bf2cd7689836e9310a3c0f6370dfb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823897"
---
# <a name="linking-to-the-remote-access-dll"></a>Vinculando à DLL de acesso remoto

Se um aplicativo for vinculado estaticamente à DLL RASAPI32, o aplicativo não será carregado se o serviço de acesso remoto não estiver instalado. Um aplicativo RAS pode ser carregado quando o RAS não é instalado usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) para carregar a dll e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter ponteiros para as funções RAS.

As funções RAS estão localizadas em RASAPI32.DLL. A biblioteca de importação para essas funções é RASAPI32. LIB. Para usar as funções RAS, seus programas devem incluir os seguintes arquivos:



| Arquivo       | Descrição                                                                 |
|------------|-----------------------------------------------------------------------------|
| Services. T      | Contém os protótipos de função RAS, constantes e definições de estrutura. |
| RASERROR. T | Contém os códigos de erro de RAS.                                               |



 

 

 