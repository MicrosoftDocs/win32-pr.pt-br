---
description: O método ProvideTextData é chamado pelo Mergemod.dll para recuperar dados de texto da ferramenta de cliente. Mergemod.dll fornece o nome da entrada correspondente na Tabela ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Método ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752661"
---
# <a name="configuremoduleprovidetextdata-method"></a>Método ConfigureModule. ProvideTextData

O método **ProvideTextData** é chamado pelo Mergemod.dll para recuperar dados de texto da ferramenta de cliente. Mergemod.dll fornece o *nome* da entrada correspondente na Tabela ModuleConfiguration.

A ferramenta deve retornar S \_ OK e fornecer o texto de personalização apropriado em ConfigData. A ferramenta de cliente é responsável por alocar os dados, mas Mergemod.dllé responsável por liberar a memória. Esse argumento deve ser um objeto **BSTR** . **LPCWSTR** não é aceito.

Se a ferramenta não fornecer dados de configuração para esse valor de *nome* , a função deverá retornar S \_ false. Nesse caso Mergemod.dll ignora o valor do argumento ConfigData e usa o valor padrão da Tabela ModuleConfiguration.

Qualquer código de retorno diferente de S \_ OK ou s \_ false fará com que um erro seja registrado (se um log estiver aberto) e resultará na falha da mesclagem.

Como essa função segue a convenção padrão **BSTR** , NULL é equivalente à cadeia de caracteres vazia.

## <a name="syntax"></a>Sintaxe


```JScript
ConfigureModule.ProvideTextData(
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

Consulte a [**função ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Mergemod.dll 2,0 ou posterior<br/>                                                    |
| parâmetro<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




