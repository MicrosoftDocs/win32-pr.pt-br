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
ms.openlocfilehash: a1521738af4411baa2c11f3d20722e09e2d22a83
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499123"
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

**GUID** que identifica um perfil conforme definido no arquivo de cabeçalho do SDK do Windows Media Format Wmsysprf. h.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores de **HRESULT** a seguir.



| Código de retorno                                                                                         | Descrição                             |
|-----------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | O método foi bem-sucedido.<br/>        |
| <dl> <dt>**E \_ falha**</dt> </dl>              | O perfil não é válido.<br/>    |
| <dl> <dt>**VFW \_ E \_ estado incorreto \_**</dt> </dl> | O grafo de filtro é interrompido.<br/> |



 

## <a name="remarks"></a>Comentários

A partir do SDK da série 9 do Windows Media Format, nenhum novo perfil de sistema foi definido. Somente os GUIDs do perfil do sistema da versão 8 (ou anterior) podem ser usados com esse método.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

