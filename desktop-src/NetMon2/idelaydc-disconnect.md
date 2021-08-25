---
description: 'IDelaydC: método isconnect:D-o método Disconnect desconecta o NPP da rede.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: 'IDelaydC: método:D isconnect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: ad24ad2557401509c1bc1e076a545f05d1c03dd79fbcf73a05d3efccfdfb8886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910666"
---
# <a name="idelaydcdisconnect-method"></a>Método IDelaydC::D isconnect

O método **Disconnect desconecta** o NPP da rede.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                          | Descrição                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>      | O NPP está capturando dados. Não é possível desconectar o NPP da rede durante uma captura.<br/>            |
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl> | O NPP não está conectado à rede.<br/>                                                               |
| <dl> <dt>**NMERR \_ não \_ atrasada**</dt> </dl>   | o NPP está conectado à rede, mas não com o método [IDelaydC:: Conexão](idelaydc-connect.md) .<br/> |



 

## <a name="remarks"></a>Comentários

Este método não pode ser chamado quando o NPP está capturando dados. Você deve chamar o método **IDelaydC:: Stop** antes de chamar **Disconnect**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC:: Conexão](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




