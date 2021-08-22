---
title: DRM_LICENSE_STATE_DATA estrutura (Wmdrmsdk.h)
description: A estrutura DE \_ DADOS DE ESTADO DE LICENÇA \_ \_ DRM contém informações sobre as restrições de licença para um direito DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA formato de mídia do Windows da estrutura
- formato de mídia de janelas de estrutura
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63ba00384ec7c3340aa099f1b427cd8953969704bd0585f0da58cd4fd0ffd6ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708926"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>DRM_LICENSE_STATE_DATA estrutura (Wmdrmsdk.h)

A **estrutura DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM** contém informações sobre as restrições de licença para um direito DRM.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwStreamId**
</dt> <dd>

Número de fluxo ao qual a licença se aplica. Deve ser 0, o que indica que a licença se aplica a todos os fluxos no arquivo.

</dd> <dt>

**dwCategory**
</dt> <dd>

Categoria de cadeia de caracteres a ser exibida. Consulte [**CATEGORIA DE ESTADO DA LICENÇA \_ \_ \_ DRM para**](drmdrm-license-state-category.md) ver os valores possíveis e seu significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de itens fornecidos em **dwCount.** Normalmente, esse valor é 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Uma matriz de 0 ou 1 ou mais valores **DWORD** que representam o número de vezes que a ação especificada em **dwCategory** pode ser executada. Consulte Observações.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de itens fornecidos em **datetime.** Normalmente, não mais do que duas datas são usadas, por exemplo, com uma licença válida de uma data até outra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Uma matriz de uma ou mais estruturas **FILETIME** que representam uma ou mais datas na licença. O significado de uma data específica depende do valor **de dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero ou mais dos seguintes sinalizadores combinados com um OR bit a **bit:**



| Sinalizador                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ LICENSE STATE DATA \_ \_ \_ LTD        | Se definido, pode haver mais licenças que se aplicam ao conteúdo. A única maneira de ter certeza sobre as licenças individuais que se aplicam a uma determinada ID de chave é enumerar as licenças. Para fazer isso, chame [**IWMDRMLicenseManagement::CreateLicenseEnumeration,**](iwmdrmlicensemanagement-createlicenseenumeration.md)passando a ID da chave como o parâmetro bstrKID. Em seguida, use a interface IWMDRMLicense recuperada para examinar as licenças. |
| OPL \_ DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM \_ PRESENTES | Se definido, a licença incluirá opLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do aplicativo.                                                                                                                                                                                                                                                                                  |
| DADOS DE \_ ESTADO \_ DE LICENÇA DRM SAP \_ \_ \_ PRESENT | Se definido, o conteúdo deverá ser entregue usando o SAP (caminho de áudio seguro).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recuperada chamando **IWMDRMLicenseQuery::QueryLicenseState.**

Se **dwCategory** for **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL**, a matriz **datetime** normalmente conterá duas datas: uma data "from" e uma data "until". Dois pares de datas também podem ser especificados para criar licenças mais complexas.

Os elementos da matriz **dwCount** correspondem às datas ou intervalos de datas especificados na **matriz datetime.** Se **dwCategory** for **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL** e **datetime** contiver um par de datas, **dwCount** conterá um elemento. Se **datetime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.

Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo. Por exemplo, eles podem ter adquirido uma licença que permitia cinco jogos até o final do mês e, posteriormente, adquiriram uma segunda licença para direitos ilimitados. Nesse caso, o sinalizador DRM LICENSE STATE DATA LIMITED é definido em \_ \_ \_ \_ **dwVague** ( ) e o componente DRM usará um algoritmo para determinar o conjunto mais provável de direitos que foram `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` aplicados. Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





