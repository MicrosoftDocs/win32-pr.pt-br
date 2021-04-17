---
title: Estrutura de DRM_LICENSE_STATE_DATA (Drmexternals. h)
description: A estrutura de dados de estado de licença do DRM \_ \_ \_ contém informações de licença sobre um direito de DRM especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- Formato de mídia do Windows de estrutura de DRM_LICENSE_STATE_DATA
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105762937"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>Estrutura de DRM_LICENSE_STATE_DATA (Drmexternals. h)

A estrutura de **dados de estado de licença do DRM \_ \_ \_** contém informações de [*licença*](wmformat-glossary.md) sobre um direito de [*DRM*](wmformat-glossary.md) especificado.

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

Categoria da cadeia de caracteres a ser exibida. Consulte [**\_ categoria de \_ estado \_ de licença do DRM**](drm-license-state-category.md) para obter os valores possíveis e seu significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de itens fornecidos em **dwCount**. Esse valor geralmente é 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Uma matriz de 0 ou 1 ou mais **DWORD** s que representa o número de vezes que a ação especificada em **dwCategory** pode ser executada. Consulte Observações.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de itens fornecidos em **DateTime**. Normalmente, no máximo duas datas são usadas, por exemplo, com uma licença que é válida de uma data até outra data.

</dd> <dt>

**data e hora \[ 4\]**
</dt> <dd>

Uma matriz de uma ou mais estruturas FILETIME que representam uma ou mais datas na licença. O significado de uma determinada data depende do valor de **dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero ou mais dos seguintes sinalizadores combinados com um **OR bit a** bit:



| Sinalizador                                    | Descrição                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| dados de estado de licença do DRM \_ \_ \_ \_ vagados        | Se definido, pode haver mais licenças que se aplicam ao conteúdo.                                                                                         |
| \_dados de estado da licença DRM \_ \_ \_ OPL \_ presentes | Se definido, a licença inclui OPLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do seu aplicativo. |
| dados de estado da licença do DRM \_ \_ \_ \_ SAP \_ presente | Se definido, o conteúdo deve ser entregue usando o caminho de áudio seguro (SAP).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é retornada (encapsulada em uma estrutura de dados de estado de licença do WM) de uma chamada para [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando você especifica uma das propriedades de estado de licença DRM. [**\_ \_ \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) Essas propriedades são:

-   [**\_Reprodução de licensestate DRM \_**](drm-licensestate-playback.md)
-   [**CopyToCD de licença do DRM \_ \_**](drm-licensestate-copytocd.md)
-   [**CopyToSDMIDevice de licença do DRM \_ \_**](drm-licensestate-copytosdmidevice.md)
-   [**CopyToNonSDMIDevice de licença do DRM \_ \_**](drm-licensestate-copytononsdmidevice.md)
-   [**CollaborativePlay de licença do DRM \_ \_**](drm-licensestate-collaborativeplay.md)
-   [**\_Cópia do licensestate do DRM \_**](drm-licensestate-copy.md)
-   [**PlaylistBurn de licença do DRM \_ \_**](drm-licensestate-playlistburn.md)

Se **dwCategory** for **a \_ \_ \_ \_ contagem de estado de licença do WM DRM \_ de \_ until,** a matriz **DateTime** normalmente conterá duas datas, uma data "de" e uma data "until". Dois pares de datas também podem ser especificados para criar licenças mais complexas.

Os elementos da matriz **dwCount** correspondem às datas ou aos intervalos de datas especificados na matriz **DateTime** . Se **dwCategory** for **a \_ \_ contagem de \_ estado de licença do WM DRM \_ \_ de \_ until** e **DateTime** contiver um par de datas, então **dwCount** conterá um elemento. Se **DateTime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.

Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo. Por exemplo, eles podem ter adquirido uma licença que permitia cinco reproduções até o fim do mês e posteriormente adquiriu uma segunda licença para direitos ilimitados. Nesse caso, o \_ sinalizador vago de dados de estado da licença DRM \_ \_ \_ é definido em **dwVague** ( `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` ) e o componente DRM usará um algoritmo para determinar o conjunto de direitos mais provável que foram aplicados. Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | SDK do Windows Media Format 7 ou versões posteriores do SDK<br/>                       |
| parâmetro<br/>                   | <dl> <dt>Drmexternals. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

