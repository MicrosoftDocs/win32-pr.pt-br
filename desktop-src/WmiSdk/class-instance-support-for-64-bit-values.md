---
description: Fornece restrições para o uso de valores de 64 bits como parte de um caminho.
ms.assetid: 63f4f6c5-7803-425d-912f-bb1dd716e617
ms.tgt_platform: multiple
title: Suporte de instância de classe para valores de 64 bits
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae778bcaad724d727bbda6d6a421ae19c562acdd50c33aa7764bea3b1861273e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556823"
---
# <a name="class-instance-support-for-64-bit-values"></a>Suporte de instância de classe para valores de 64 bits

Você pode usar um valor de chave de 64 bits como parte de um caminho, com as seguintes restrições:

-   Desde que você não exceda o intervalo de 32 bits, você pode atribuir e recuperar valores da chave como faria com uma propriedade de 32 bits.
-   Depois de exceder o valor inteiro de 0x7FFFFFFF (para tipos assinados), 0x80000000 (para tipos não assinados) ou 32 bits, você deve usar aspas.
-   O único caminho válido para um valor de 64 bits está localizado nas propriedades **\_ \_ RelPath** ou **\_ \_ Path** da instância. Como tal, o WMI não oferece suporte à notação hexadecimal para o valor equivalente.
-   Se o WMI registra a chave de instância como um número negativo, você deve usar o número original para recuperar a instância.

A semântica de consulta não é afetada e se comporta conforme o esperado. Esse comportamento afeta apenas as operações caminho do objeto, [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)e [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

O exemplo a seguir mostra que as instâncias de classe podem ter valores de chave de 64 bits.

``` syntax
class MyBig
{
  [key] sint64 k;
  sint64 p;
};

instance of MyBig
{
  k = 2;
  p = 3;
};
```

 

 



