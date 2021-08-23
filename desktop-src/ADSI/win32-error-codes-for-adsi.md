---
title: Códigos de erro do Win32 para ADSI
description: Códigos de erro Win32 padrão também são usados para retornar mensagens de erro ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de erro do Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b18539e93504991f244bbba8b41b13e524ff236918145deda73788169cef368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589736"
---
# <a name="win32-error-codes-for-adsi"></a>Códigos de erro do Win32 para ADSI

Códigos de erro Win32 padrão também são usados para retornar mensagens de erro ADSI. Especificamente, o provedor ADSI LDAP mapeia todos os códigos de erro LDAP para códigos de erro win32. Os **valores HRESULT** desses códigos de erro são do formato 0x8007XXXX, em que os últimos quatro dígitos hexadecimais, XXXX, correspondem aos valores **DWORD** do código de erro Win32 apropriado. Por exemplo, o valor do erro ADSI 0x80072020 fornece o valor de erro Win32 de 0x2020 em hexadecimal ou 8224 em decimal.

Para converter o **valor HRESULT** de um código de erro ADSI, retornado pelo seu aplicativo, para o valor **DWORD** de erro do Win32 correspondente, conforme definido nos arquivos de título acima, use o procedimento a seguir.

A maioria dos códigos de erro do Win32 para ADSI é definida em Winerror.h ou Error.h. Os valores de erro são listados como valores decimais nesses arquivos.

**Para converter o **valor HRESULT** de um código de erro ADSI no valor **DWORD** do erro Win32 correspondente**

1.  Converta **o valor HRESULT** em um número hexadecimal se começar com um valor decimal como você pode obter de um Visual Basic aplicativo.
2.  Solte a 0x8007 parte produzir o restante.
3.  Converta o restante em um número decimal.
4.  Procure o restante decimal em Winerror.h.
5.  Se não for encontrado em Winerror.h, subtraia 2100 do restante decimal e procure o resultado em Decimal.h.

A ADSI 2.0 mapeia os códigos de erro LDAP para um conjunto de códigos de erro Win32 que é diferente do usado no ADSI para o Windows 2000 e o Cliente DS. As diferenças estão listadas em:

-   [Códigos de erro do Win32](win32-error-codes.md)
-   [Códigos de erro do Win32 para ADSI 2.0](win32-error-codes-for-adsi-2-0.md)

 

 




