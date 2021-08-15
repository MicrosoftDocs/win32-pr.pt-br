---
title: Método IConfigAsfWriter ConfigureFilterUsingProfileGuid
description: O método ConfigureFilterUsingProfileGuid configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado. (Preterido.).
ms.assetid: 94161ee7-1b74-47af-9d77-568abe6237c3
keywords:
- Formato de mídia do windows do método ConfigureFilterUsingProfileGuid
- ConfigureFilterUsingProfileGuid method windows Media Format , interface IConfigAsfWriter
- Formato de mídia da interface IConfigAsfWriter , método ConfigureFilterUsingProfileGuid
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
# <a name="iconfigasfwriterconfigurefilterusingprofileguid-method"></a>Método IConfigAsfWriter::ConfigureFilterUsingProfileGuid

O **método ConfigureFilterUsingProfileGuid** configura o filtro para gravar um arquivo ASF com base no perfil predefinido especificado. (Preterido.)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ConfigureFilterUsingProfileGuid(
  [in] REFGUID guidProfile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*guidProfile* \[ Em\]
</dt> <dd>

**GUID** identificando um perfil conforme definido no arquivo de Windows do SDK de Formato de Mídia Wmsysprf.h.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos seguintes **valores HRESULT.**



| Código de retorno                                                                                         | Descrição                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ FAIL**</dt> </dl>              | O perfil não é válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ ESTADO \_ ERRADO**</dt> </dl> | O grafo de filtro é interrompido.<br/> |



 

## <a name="remarks"></a>Comentários

A partir do SDK Windows Media Format 9 Series, nenhum novo perfil do sistema foi definido. Somente guids de perfil do sistema versão 8 (ou anterior) podem ser usados com esse método.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

