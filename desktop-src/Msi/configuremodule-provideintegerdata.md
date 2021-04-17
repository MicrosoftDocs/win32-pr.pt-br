---
description: O método ProvideIntegerData do objeto ConfigureModule é chamado por Mergemod.dll para recuperar dados inteiros da ferramenta de cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule. ProvideIntegerData (Mergemod. h)
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
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757127"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Método ConfigureModule. ProvideIntegerData

O método **ProvideIntegerData** do [**objeto ConfigureModule**](configuremodule-object.md) é chamado por Mergemod.dll para recuperar dados inteiros da ferramenta de cliente.

Mergemod.dll fornece o *nome* da entrada correspondente na [Tabela ModuleConfiguration](moduleconfiguration-table.md).

A ferramenta deve retornar S \_ OK e fornecer o inteiro de personalização apropriado em *ConfigData*.

Se a ferramenta não fornecer dados de configuração para esse valor de *nome* , a função deverá retornar S \_ false. Nesse caso Mergemod.dll ignora o valor do argumento *ConfigData* e usa o valor padrão da Tabela ModuleConfiguration.

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

Ponteiro para texto de personalização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O cliente pode ser chamado não mais de uma vez para cada registro na [Tabela ModuleConfiguration](moduleconfiguration-table.md). Observe que Mergemod.dll nunca faz várias chamadas para o cliente para o mesmo valor de "nome". Se nenhum registro na tabela ModuleSubstitution usar a propriedade, uma entrada na Tabela ModuleConfiguration não fará chamadas para o cliente.

### <a name="c"></a>C++

Consulte a [**função ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




