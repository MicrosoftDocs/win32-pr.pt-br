---
description: Descreve o processo de criação de um aplicativo WSDAPI usando o WsdCodeGen.
ms.assetid: 8f172e2c-4cd1-4108-9c8d-01a731aca83b
title: Usando WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6395d39a84415cc56e66949ea82ef7a1acd9fc009b7e1b2c93fa2712e8a81a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463166"
---
# <a name="using-wsdcodegen"></a>Usando WsdCodeGen

**Para compilar um aplicativo WSDAPI usando WsdCodeGen**

1.  Defina o contrato funcional para o host do dispositivo em um arquivo WSDL.
2.  Gere um arquivo de configuração usando WsdCodeGen. Para obter mais informações, consulte [arquivo de configuração WsdCodeGen](wsdcodegen-configuration-file.md) e [sintaxe de linha de comando WsdCodeGen](wsdcodegen-command-line-syntax.md).
3.  Abra o arquivo de configuração gerado e modifique o arquivo conforme necessário. Se você estiver criando um aplicativo cliente, pouca ou nenhuma modificação será necessária. Se você estiver criando um aplicativo host, altere os elementos de configuração específicos do usuário (como [**manufacturer**](manufacturer.md) e [**ModelName**](modelname.md)).
4.  Gere código usando WsdCodeGen, fornecendo o arquivo de configuração como entrada. Para obter mais informações, consulte [sintaxe de linha de comando WsdCodeGen](wsdcodegen-command-line-syntax.md).
5.  Use o código gerado para criar um cliente, host ou ambos.

o SDK do Windows inclui alguns arquivos WSDL de exemplo, arquivos de configuração WsdCodeGen e código gerado. Para obter mais informações, consulte [exemplos de WSDAPI](wsdapi-samples.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 



