---
description: O método configure envia informações de configuração para uma captura.
ms.assetid: b8cbbae1-3c07-489f-8e8f-77c95ec03209
title: 'Método IESP:: Configure (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 53efbe7eb2887165dacc4cb904822de953b84017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780858"
---
# <a name="iespconfigure-method"></a>Método IESP:: Configure

O método **Configure** envia informações de configuração para uma captura.

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

Identificador para o BLOB que o chamador configura.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que contém informações adicionais sobre o erro. Para obter informações sobre o conteúdo de um BLOB de erro, consulte a seção comentários neste tópico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro:



| Código de retorno                                                                                                         | Descrição                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ não \_ conectado**</dt> </dl>                | O NPP não está conectado à rede.<br/>                                                                                                                                                               |
| <dl> <dt>**NMERR \_ não \_ ESP**</dt> </dl>                      | O NPP está conectado à rede, mas não com o método [IESP:: Connect](iesp-connect.md) .<br/>                                                                                                         |
| <dl> <dt>**captura de NMERR \_**</dt> </dl>                     | O NPP relata que a sessão de captura foi iniciada.<br/>                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ gatilho ilegal**</dt> </dl>              | A parte do gatilho do BLOB de configuração está corrompida.<br/>                                                                                                                                              |
| <dl> <dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt> </dl> | O BLOB de configuração especificado por *hConfigurationBlob* não tem uma entrada necessária para executar esta operação. Examine o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.<br/> |
| <dl> <dt>**\_erro de \_ conversão de blob NMERR \_**</dt> </dl>       | O BLOB está corrompido.<br/>                                                                                                                                                                                   |
| <dl> <dt>**\_blob NMERR \_ não \_ inicializado**</dt> </dl>        | O método **createBlob** não foi chamado.<br/>                                                                                                                                                         |
| <dl> <dt>**NMERR \_ \_ blob inválido**</dt> </dl>                 | O objeto que é apontado não é um BLOB.<br/>                                                                                                                                                           |
| <dl> <dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt> </dl>         | A cadeia de caracteres não é terminada em nulo.<br/>                                                                                                                                                                     |
| <dl> <dt>**BLOB de upNMERR de \_ nível \_**</dt> </dl>                 | O número de versão do BLOB está incorreto.<br/>                                                                                                                                                                  |
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl>               | Não havia memória disponível. Desligue o Windows para liberar recursos.<br/>                                                                                                                                       |
| <dl> <dt>**\_tempo limite de NMERR**</dt> </dl>                       | O tempo limite da solicitação foi atingido.<br/>                                                                                                                                                                             |



 

## <a name="remarks"></a>Comentários

Você deve aplicar esse método para reiniciar um NPP que foi iniciado e interrompido, mas não desconectado.

O BLOB de erro retornado pelo parâmetro *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de configuração especificado em *hConfigurationBlob*. O BLOB de erro retornado contém informações de erro que o aplicativo pode usar para solução de problemas. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



 

 




