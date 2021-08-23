---
title: opção/n
description: A opção/n especifica a profundidade da composição para compor arquivos de metadados.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n alternar MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3e9575995d80a4c61b5e91be7c5cfc1c802abed892af8cfa653f62c66e602b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430966"
---
# <a name="n-switch"></a>opção/n

A opção **/n** especifica a profundidade da composição para compor arquivos de metadados.

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a>Opções de comutação

<dl> <dt>

*profundidade do namespace \_* 
</dt> <dd>

Especifica a profundidade do namespace a ser redigida em um único arquivo de metadados.

</dd> </dl>

## <a name="remarks"></a>Comentários

Aqui estão os formatos de valor possíveis que você pode especificar com a opção **/n** .



| Formato de valor                   | Descrição                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| Int32 > 0                   | Compor todos os tipos na profundidade do namespace especificada na opção.               |
| -1                             | Compor todos os tipos em um arquivo IDL por namespace.                              |
| <namespace>: Int32 > 0 | Compor todos os tipos com namespace correspondente na profundidade especificada na opção. |
| <namespace>:-1           | Compor todos os tipos com namespace correspondente em um arquivo por namespace.          |



 

A tabela a seguir mostra os resultados de diferentes combinações da opção **/n** trabalhando nesses namespaces.

-   Windows. Foundation. Collections. IIterable
-   Windows. Conectável. DirectUI. Controls. Button
-   Windows. Conectável. DirectUI. Controls. ListView
-   Windows. Conectável. Envolvendo. de aplicativo. Playto. destino
-   Windows. Web. Syndication. RSS



| Opções                         | Result                                                                                                                                                                                                                                                       | Explicação                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/n:-1**  / **n:1**               | Windows.winmd                                                                                                                                                                                                                                                | A última opção/n substitui todas as opções-n anteriores.                                                                                                                                                                                                                                                                           |
| **/n:-1/n: Windows. INTERFACE DO USUÁRIO: 2**         | <dl> <dt>Windows. Windows Foundation. winmd</dt> <dt>. Windows UI. winmd</dt> <dt>. Web. Syndication. winmd</dt> </dl> | <dl> <dt>**Windows. A base** é sempre composta em – n:2.</dt> <dt>**Windows. Os tipos de interface do usuário** são agrupados.</dt> <dt>**Windows. Web. Syndication** é composto em n:-1.</dt> </dl>       |
| **/n: 1/n: Windows. Conectável. DirectUI: 3** | <dl> <dt>Windows. Windows Foundation. winmd</dt> <dt>. Conectável. DirectUI. winmd</dt> <dt>Windows. winmd</dt> </dl>       | <dl> <dt>**Windows. A base** é sempre composta em – n:2.</dt> <dt>**Windows. Conectável. DirectUI** é composto no nível 3.</dt> <dt>Todos os outros tipos são compostos no nível 1.</dt> </dl> |



 

Aqui estão as regras para lidar com várias instâncias da opção **/n** .

-   A instância mais específica prevalece. Por exemplo, se você especificar **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE resolverá a. b. c. D no nível 4, porque A. b. c é mais específica que A.B. A. B. E. F resolve na profundidade 5, porque corresponde A. B, mas não A.B.C.
-   A última instância prevalece. Por exemplo, se você especificar **– n:5 – n:2**, os tipos serão compostos no nível 2.
-   Ambas as regras se aplicam. Se você especificar – n:A.B.C: 4 – n:A.B.C: 1, namespace A. B. C é composto no nível 1.

## <a name="examples"></a>Exemplos

**mdmerge.exe-metadados \_ dir $ (caminho de metadados do SDK \_ \_ )-i $ ( \_ caminho de metadados do SDK interno \_ \_ )-o $ (caminho do obj \_ ) \\ $O \\ SystemMetadata-v-n:-1-n: Windows. Fundação: 2**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------|
| Cliente<br/> | Windows 8<br/>           |
| Servidor<br/> | Windows Server 2012<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





