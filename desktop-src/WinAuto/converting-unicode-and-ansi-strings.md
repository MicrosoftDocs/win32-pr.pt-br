---
title: Convertendo cadeias de caracteres Unicode e ANSI
description: O Microsoft Acessibilidade Ativa usa cadeias de caracteres Unicode, conforme definido pelo tipo de dados BSTR.
ms.assetid: 47f525fe-6d18-43b9-a706-e49afa796830
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fa26813c61be0a3959593f370016cfce0211ea9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294276"
---
# <a name="converting-unicode-and-ansi-strings"></a>Convertendo cadeias de caracteres Unicode e ANSI

O Microsoft Acessibilidade Ativa usa cadeias de caracteres Unicode, conforme definido pelo tipo de dados **BSTR** . Se seu aplicativo não usar cadeias de caracteres Unicode ou se você quiser converter cadeias de caracteres para determinadas chamadas de API, use as funções do Microsoft Win32 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) e [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para executar a conversão necessária.

Use [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) para converter uma cadeia de caracteres Unicode em uma cadeia de caracteres ANSI. A função [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) converte uma cadeia de caracteres ANSI em uma cadeia de caracteres Unicode.

Use [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) e [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) para alocar e liberar tipos de dados **BSTR** .

Para obter mais informações sobre essas funções de cadeia de caracteres, consulte suas referências no SDK (Software Development Kit) do Windows.

 

 