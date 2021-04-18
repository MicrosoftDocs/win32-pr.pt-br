---
title: Estrutura de DRM_LICENSE_STATE_DATA (wmdrmsdk. h)
description: A estrutura de dados de estado de licença do DRM \_ \_ \_ contém informações sobre as restrições de licença para um direito de DRM.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- Formato de mídia do Windows de estrutura de DRM_LICENSE_STATE_DATA
- estruturar formato de mídia do Windows
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
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814009"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a>Estrutura de DRM_LICENSE_STATE_DATA (wmdrmsdk. h)

A estrutura de dados de estado de licença do DRM contém informações sobre as restrições de licença para um direito de DRM. **\_ \_ \_**

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

Categoria da cadeia de caracteres a ser exibida. Consulte [**\_ categoria de \_ estado \_ de licença do DRM**](drmdrm-license-state-category.md) para obter os valores possíveis e seu significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de itens fornecidos em **dwCount**. Esse valor geralmente é 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Uma matriz de 0 ou 1 ou mais valores **DWORD** que representam o número de vezes que a ação especificada em **dwCategory** pode ser executada. Consulte Observações.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de itens fornecidos em **DateTime**. Normalmente, no máximo duas datas são usadas, por exemplo, com uma licença que é válida de uma data até outra data.

</dd> <dt>

**data e hora \[ 4\]**
</dt> <dd>

Uma matriz de uma ou mais estruturas **FILETIME** que representam uma ou mais datas na licença. O significado de uma determinada data depende do valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero ou mais dos seguintes sinalizadores combinados com um **OR bit a** bit:



| Sinalizador                                    | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dados de estado de licença do DRM \_ \_ \_ \_ vagados        | Se definido, pode haver mais licenças que se aplicam ao conteúdo. A única maneira de ter certeza sobre as licenças individuais que se aplicam a uma determinada ID de chave é enumerar as licenças. Para fazer isso, chame [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando a ID da chave como o parâmetro bstrKID. Em seguida, use a interface IWMDRMLicense recuperada para examinar as licenças. |
| \_dados de estado da licença DRM \_ \_ \_ OPL \_ presentes | Se definido, a licença inclui OPLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do seu aplicativo.                                                                                                                                                                                                                                                                                  |
| dados de estado da licença do DRM \_ \_ \_ \_ SAP \_ presente | Se definido, o conteúdo deve ser entregue usando o caminho de áudio seguro (SAP).                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é recuperada chamando **IWMDRMLicenseQuery:: QueryLicenseState**.

Se **dwCategory** for **a \_ \_ \_ \_ contagem de estado de licença do WM DRM \_ de \_ until**, a matriz **DateTime** normalmente conterá duas datas: uma data "de" e uma data "until". Dois pares de datas também podem ser especificados para criar licenças mais complexas.

Os elementos da matriz **dwCount** correspondem às datas ou aos intervalos de datas especificados na matriz **DateTime** . Se **dwCategory** for **a \_ \_ contagem de \_ estado de licença do WM DRM \_ \_ de \_ until** e **DateTime** contiver um par de datas, então **dwCount** conterá um elemento. Se **DateTime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.

Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo. Por exemplo, eles podem ter adquirido uma licença que permitia cinco reproduções até o fim do mês e posteriormente adquiriu uma segunda licença para direitos ilimitados. Nesse caso, o \_ sinalizador vago de dados de estado da licença DRM \_ \_ \_ é definido em **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e o componente DRM usará um algoritmo para determinar o conjunto de direitos mais provável que foram aplicados. Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](drm-structures.md)
</dt> </dl>

 

 





