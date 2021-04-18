---
description: Recupera um número especificado de bytes aleatórios do gerador de número aleatório do sistema.
ms.assetid: 04746229-9dc1-4748-80c1-f1960bd1b768
title: Função SystemPrng
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemPrng
api_type:
- DllExport
api_location:
- Ksecdd.sys
- Cng.sys
ms.openlocfilehash: d847d34ffd11e158170f55599de0ceb3acf3c697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758925"
---
# <a name="systemprng-function"></a>Função SystemPrng

\[O **SystemPrng** está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, use [**BCryptGenRandom**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgenrandom).\]

A função **SystemPrng** recupera um número especificado de bytes aleatórios do gerador de números aleatórios do sistema.

> [!Note]  
> Esta função não tem nenhum arquivo de cabeçalho ou biblioteca de importação associado. Para chamar essa função, você deve criar um arquivo de cabeçalho definido pelo usuário.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL SystemPrng(
  _Out_ unsigned char pbRandomData,
  _In_  size_t        cbRandomData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pbRandomData* \[ fora\]
</dt> <dd>

Um ponteiro para um buffer que recebe os bytes recuperados.

</dd> <dt>

*cbRandomData* \[ no\]
</dt> <dd>

O número de bytes a serem recuperados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista com SP1\]<br/>                                                                                                                                                                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys no Windows Server 2008 e no Windows Vista com SP1; </dt> <dt>Cng.sys no Windows 7 e no Windows Server 2008 R2</dt> </dl> |



 

 




