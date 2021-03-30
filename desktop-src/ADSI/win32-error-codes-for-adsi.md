---
title: Códigos de erro do Win32 para ADSI
description: Os códigos de erro padrão do Win32 também são usados para retornar mensagens de erro ADSI.
ms.assetid: 5b7b85c9-ccca-4ea3-8b37-54f6b30a509f
ms.tgt_platform: multiple
keywords:
- Códigos de erro do Win32 para ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47151a3a1619a7f224dc0b9b7f0871813a346a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634851"
---
# <a name="win32-error-codes-for-adsi"></a>Códigos de erro do Win32 para ADSI

Os códigos de erro padrão do Win32 também são usados para retornar mensagens de erro ADSI. Especificamente, o provedor de LDAP ADSI mapeia todos os códigos de erro LDAP para códigos de erro do Win32. Os valores **HRESULT** desses códigos de erro são do formato 0x8007XXXX, em que os últimos quatro dígitos hexadecimais, xxxx, correspondem aos valores **DWORD** do código de erro Win32 apropriado. Por exemplo, o valor de erro ADSI 0x80072020 fornece o valor de erro Win32 de 0x2020 em hexadecimal ou 8224 em decimal.

Para converter o valor **HRESULT** de um código de erro ADSI, retornado pelo seu aplicativo, para o valor de **DWORD** de erro do Win32 correspondente, conforme definido nos arquivos de cabeçalho acima, use o procedimento a seguir.

A maioria dos códigos de erro do Win32 para ADSI está definida em Winerror. h ou Lmerr. h. Os valores de erro são listados como valores decimais nesses arquivos.

**Para converter o valor **HRESULT** de um código de erro ADSI para o valor de **DWORD** de erro Win32 correspondente**

1.  Converta o valor **HRESULT** em um número hexadecimal se estiver começando com um valor decimal, pois você pode obter de um aplicativo Visual Basic.
2.  Descartar a parte 0x8007 produzir o restante.
3.  Converta o resto em um número decimal.
4.  Pesquisar o restante decimal em Winerror. h.
5.  Se não for encontrado em Winerror. h, subtraia 2100 do restante decimal e procure o resultado em Lmerr. h.

O ADSI 2,0 mapeia os códigos de erro LDAP para um conjunto de códigos de erro do Win32 que é diferente daquele usado na ADSI para o Windows 2000 e o cliente DS. As diferenças são listadas em:

-   [Códigos de erro do Win32](win32-error-codes.md)
-   [Códigos de erro do Win32 para ADSI 2,0](win32-error-codes-for-adsi-2-0.md)

 

 




