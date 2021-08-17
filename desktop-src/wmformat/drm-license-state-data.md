---
title: DRM_LICENSE_STATE_DATA estrutura (Drmexternals.h)
description: A estrutura DE \_ DADOS DE ESTADO DE LICENÇA \_ \_ DRM contém informações de licença sobre um direito DRM especificado.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA formato de mídia do Windows
- formato de mídia de janelas de estrutura
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
ms.openlocfilehash: 3e6703481dc1d3608a8bf08ab2bbd216db4a9ecdc91bd4604d2b9de7d7de4fa3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848529"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a>DRM_LICENSE_STATE_DATA estrutura (Drmexternals.h)

A **estrutura DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM** [*contém*](wmformat-glossary.md) informações de licença sobre um direito [*DRM*](wmformat-glossary.md) especificado.

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

Categoria de cadeia de caracteres a ser exibida. Consulte [**CATEGORIA DE ESTADO DA LICENÇA \_ \_ \_ DRM para**](drm-license-state-category.md) ver os valores possíveis e seu significado.

</dd> <dt>

**dwNumCounts**
</dt> <dd>

Número de itens fornecidos em **dwCount.** Normalmente, esse valor é 0 ou 1.

</dd> <dt>

**dwCount \[ 4\]**
</dt> <dd>

Uma matriz de 0 ou 1 ou mais **DWORDs** que representam o número de vezes que a ação especificada em **dwCategory** pode ser executada. Consulte Observações.

</dd> <dt>

**dwNumDates**
</dt> <dd>

Número de itens fornecidos em **datetime.** Normalmente, não mais do que duas datas são usadas, por exemplo, com uma licença válida de uma data até outra.

</dd> <dt>

**datetime \[ 4\]**
</dt> <dd>

Uma matriz de uma ou mais estruturas FILETIME que representam uma ou mais datas na licença. O significado de uma data específica depende do valor **de dwCategory**.

</dd> <dt>

**dwVague**
</dt> <dd>

Zero ou mais dos seguintes sinalizadores combinados com um OR bit a **bit:**



| Sinalizador                                    | Descrição                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRM \_ LICENSE STATE DATA \_ \_ \_ LTD        | Se definido, pode haver mais licenças que se aplicam ao conteúdo.                                                                                         |
| OPL \_ DE DADOS DE ESTADO DE LICENÇA \_ \_ \_ DRM \_ PRESENTES | Se definido, a licença incluirá opLs (níveis de proteção de saída) que devem ser recuperados e verificados em relação ao destino da saída do aplicativo. |
| DADOS DE \_ ESTADO \_ DE LICENÇA DRM SAP \_ \_ \_ PRESENT | Se definido, o conteúdo deverá ser entregue usando o SAP (caminho de áudio seguro).                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura é retornada (encapsulada em uma estrutura [**WM \_ LICENSE STATE \_ \_ DATA)**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) de uma chamada para [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) quando você especifica uma das propriedades de estado da licença DRM. Essas propriedades são:

-   [**Reprodução \_ de LicenseState drm \_**](drm-licensestate-playback.md)
-   [**DRM \_ LicenseState \_ CopyToCD**](drm-licensestate-copytocd.md)
-   [**DRM \_ LicenseState \_ CopyToSDMIDevice**](drm-licensestate-copytosdmidevice.md)
-   [**DRM \_ LicenseState \_ CopyToNonSDMIDevice**](drm-licensestate-copytononsdmidevice.md)
-   [**DRM \_ LicenseState \_ CollaborativePlay**](drm-licensestate-collaborativeplay.md)
-   [**Cópia de LicenseState do DRM \_ \_**](drm-licensestate-copy.md)
-   [**PlaylistState \_ LicenseState \_ drm**](drm-licensestate-playlistburn.md)

Se **dwCategory** for **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL,** a matriz **datetime** normalmente conterá duas datas, uma data "from" e uma data "until". Dois pares de datas também podem ser especificados para criar licenças mais complexas.

Os elementos da matriz **dwCount** correspondem às datas ou intervalos de datas especificados na **matriz datetime.** Se **dwCategory** for **WM \_ DRM LICENSE STATE COUNT \_ FROM \_ \_ \_ \_ UNTIL** e **datetime** contiver um par de datas, **dwCount** conterá um elemento. Se **datetime** contiver dois pares de data (quatro elementos), **dwCount** deverá conter dois elementos, um para cada par de datas.

Em alguns casos, os usuários podem ter sido emitidos mais de uma licença para um arquivo. Por exemplo, eles podem ter adquirido uma licença que permitia cinco jogos até o final do mês e, posteriormente, adquiriram uma segunda licença para direitos ilimitados. Nesse caso, o sinalizador DRM LICENSE STATE DATA LIMITED é definido em \_ \_ \_ \_ **dwVague** ( ) e o componente DRM usará um algoritmo para determinar o conjunto mais provável de direitos que foram `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` aplicados. Quando uma licença expirar, o componente DRM examinará as licenças restantes e assim por diante até que todas as licenças tenham expirado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                      |
| Versão<br/>                  | Windows SDK de Formato de Mídia 7 ou versões posteriores do SDK<br/>                       |
| Cabeçalho<br/>                   | <dl> <dt>Drmexternals.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas**](structures.md)
</dt> </dl>

 

