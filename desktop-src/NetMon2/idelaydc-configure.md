---
description: O método configure envia informações de configuração usadas para uma captura.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Método IDelaydCConfigure (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460958"
---
# <a name="idelaydcconfigure-method"></a>Método IDelaydC:: Configure

O método **Configure** envia informações de configuração usadas para uma captura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hConfigurationBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB que contém as informações de configuração.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que contém informações adicionais sobre o erro. Para obter informações sobre o conteúdo de um BLOB de erro, consulte a seção comentários neste tópico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                      | Descrição                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**captura de NMERR \_**</dt> </dl>                  | O NPP relata que a sessão de captura foi iniciada.<br/>                          |
| <dl> <dt>**\_disco NMERR \_ não \_ local \_ fixo**</dt> </dl>    |                                                                                           |
| <dl> <dt>**NMERR \_ \_ não pôde \_ criar \_ memória**</dt> </dl> |                                                                                           |
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl>            | Não havia memória disponível. Desligue o Windows para liberar recursos.<br/>               |
| <dl> <dt>**NMERR \_ \_ parâmetro inválido**</dt> </dl>         | O BLOB de configuração especificado pelo parâmetro hConfiguration não é válido.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve aplicar esse método para reiniciar um NPP que tenha sido iniciado, interrompido, mas não desconectado.

O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*. O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.

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

[IDelaydC:: conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC:: iniciar](idelaydc-start.md)
</dt> <dt>

[IDelaydC:: Stop](idelaydc-stop.md)
</dt> </dl>

 

 




