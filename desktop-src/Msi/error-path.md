---
description: no Windows Installer versões 1,0 e 1,1, a propriedade Path é sempre a cadeia de caracteres vazia. Versões futuras podem usar esse valor para retornar o caminho para o arquivo ou diretório que não pôde ser criado.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Erro. propriedade Path (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7787fcd5bad5550b933b2a866308c1d5b77dd24f60fce23ebc3b227829528307
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378147"
---
# <a name="errorpath-property"></a>Propriedade Error. Path

no Windows Installer versões 1,0 e 1,1, a propriedade Path é sempre a cadeia de caracteres vazia. Versões futuras podem usar esse valor para retornar o caminho para o arquivo ou diretório que não pôde ser criado.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
propVal = Error.Path
```



## <a name="property-value"></a>Valor da propriedade

## <a name="remarks"></a>Comentários

Esse valor só é válido para erros do tipo msmErrorFileCreate ou msmErrorDirCreate. Você pode determinar o tipo de erro chamando a propriedade [**Type**](error-type.md) do objeto [**Error**](error-object.md) .

### <a name="c"></a>C++

Consulte a função [**obter \_ caminho**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 1,0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

