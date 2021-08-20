---
description: O método ProvideIntegerData do objeto ConfigureModule é chamado pelo Mergemod.dll para recuperar dados inteiros da ferramenta cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule.ProvideIntegerData (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 96472a13902322d940dc7e756c3639f9befaf6764b3ede8521f27a885a50e8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143685"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Método ConfigureModule.ProvideIntegerData

O **método ProvideIntegerData** do [**objeto ConfigureModule**](configuremodule-object.md) é chamado por Mergemod.dll para recuperar dados inteiros da ferramenta cliente.

Mergemod.dll fornece o *Nome* da entrada correspondente na [tabela ModuleConfiguration](moduleconfiguration-table.md).

A ferramenta deve retornar S OK e fornecer o inteiro de \_ personalização apropriado em *ConfigData.*

Se a ferramenta não fornecer dados de configuração para esse *valor name,* a função deverá retornar S \_ FALSE. Nesse caso, Mergemod.dll ignora o valor do argumento *ConfigData* e usa o valor Padrão da tabela ModuleConfiguration.

## <a name="syntax"></a>Sintaxe


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* 
</dt> <dd>

Nome do item para o qual os dados estão sendo recuperados.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Ponteiro para o texto de personalização.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O cliente pode ser chamado não mais de uma vez para cada registro na [tabela ModuleConfiguration](moduleconfiguration-table.md). Observe que Mergemod.dll faz várias chamadas ao cliente para o mesmo valor de "Nome". Se nenhum registro na tabela ModuleSubstitution usar a propriedade , uma entrada na tabela ModuleConfiguration não causará nenhuma chamada ao cliente.

### <a name="c"></a>C++

Consulte [**a função ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2.0 ou posterior<br/>                                                    |
| Cabeçalho<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




