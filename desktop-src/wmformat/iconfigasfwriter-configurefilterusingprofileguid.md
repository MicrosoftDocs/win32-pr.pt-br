---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: O método ConfigureFilterUsingProfileGuid configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado. (Preterido.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Formato de mídia do Windows do método ConfigureFilterUsingProfileGuid
- Método ConfigureFilterUsingProfileGuid Windows Media Format, interface IConfigAsfWriter
- Formato de mídia do Windows de interface IConfigAsfWriter, método ConfigureFilterUsingProfileGuid
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfileGuid
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f427dc67695ebaca3e3e7502f2f1961b738a8f775ace394948ef445f3ad9a64e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118703082"
---
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Método IConfigAsfWriter:: ConfigureFilterUsingProfileGuid

O método **ConfigureFilterUsingProfileGuid** configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado. (Preterido.)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidProfile* \[ no\]
</dt> <dd>

**GUID** que identifica um perfil conforme definido no arquivo de cabeçalho Windows Media Format SDK Wmsysprf. h.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                         | Descrição                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ falha**</dt> </dl>              | O perfil não é válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl> | O grafo de filtro é interrompido.<br/> |



 

## <a name="remarks"></a>Comentários

a partir do SDK do Windows Media Format 9 Series, nenhum perfil de sistema novo foi definido. Somente os GUIDs do perfil do sistema da versão 8 (ou anterior) podem ser usados com esse método.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

