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
ms.openlocfilehash: eae1a46b43278c836ff6ce318dfdce7302bb0e052664a7326f9043a60eec72d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118905625"
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

## <a name="return-value"></a>Valor retornado

Sempre retorna **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista com SP1\]<br/>                                                                                                                                                                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                                                                                                                                                           |
| DLL<br/>                      | <dl> <dt>Ksecdd.sys no Windows Server 2008 e Windows Vista com SP1;</dt> <dt>Cng.sys no Windows 7 e no Windows Server 2008 R2</dt> </dl> |



 

 




