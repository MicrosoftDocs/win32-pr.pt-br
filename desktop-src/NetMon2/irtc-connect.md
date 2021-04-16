---
description: O método Connect conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.
ms.assetid: d017c2a3-a832-4084-b21b-0cca428c5360
title: 'Método IRTC:: Connect (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.Connect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: a14e34aeb0be30165aa18ddc7da18028d715be01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757755"
---
# <a name="irtcconnect-method"></a>Método IRTC:: Connect

O método **Connect** conecta o NPP à rede usando uma NIC especificada e fornece informações de configuração para a conexão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT STDMETHODCALLTYPE Connect(
  [in]  HBLOB  hInputBlob,
  [in]  LPVOID StatusCallbackProc,
  [in]  LPVOID FramesCallbackProc,
  [in]  LPVOID UserContext,
  [out] HBLOB  hErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hInputBlob* \[ no\]
</dt> <dd>

Identificador para o BLOB que especifica a NIC à qual você está se conectando e as informações de configuração para essa conexão.

</dd> <dt>

*StatusCallbackProc* \[ no\]
</dt> <dd>

Endereço da função de retorno de chamada de status do usuário, que recebe atualizações de status, como gatilhos. Esse parâmetro pode ser definido como **nulo**.

</dd> <dt>

*FramesCallbackProc* \[ no\]
</dt> <dd>

Endereço da função de retorno de chamada de quadro do usuário, que é usada para receber atualizações de status, como gatilhos. Esse parâmetro pode ser definido como **nulo**.

</dd> <dt>

*UserContext* \[ no\]
</dt> <dd>

Valor passado quando a função de retorno de chamada de status e quadro do usuário é chamada. Se ambas as funções de retorno de chamada forem especificadas, elas deverão usar o mesmo valor de contexto do usuário. O valor desse parâmetro é normalmente o HWND ou um ponteiro ' this '.

</dd> <dt>

*hErrorBlob* \[ fora\]
</dt> <dd>

Identificador para um BLOB de erro que contém informações adicionais sobre o erro. Consulte os comentários na parte inferior deste tópico para obter informações sobre o que está no BLOB de erros.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem-sucedido, o valor de retorno será NMERR com \_ êxito.

Se o método não for bem-sucedido, o valor de retorno será um dos seguintes códigos de erro (que incluem os erros retornados pela chamada interna **IRTC:: Configure** ):



| Código de retorno                                                                                                         | Description                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ já \_ conectado**</dt> </dl>            | Esta instância do objeto COM NPP já está conectada à rede.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**\_erro de \_ conversão de blob NMERR \_**</dt> </dl>       | O BLOB de configuração está corrompido. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**a \_ entrada de blob NMERR não \_ \_ \_ \_ existe**</dt> </dl> | O BLOB de entrada especificado pelo parâmetro *hInputBlob* não tem uma entrada necessária para executar esta operação. Esse erro pode ser gerado pela chamada **IRTC:: Connect** ou **IRTC:: Configure** . Examine o BLOB de erro retornado por *hErrorBlob* para determinar qual entrada não foi encontrada.<br/> |
| <dl> <dt>**\_blob NMERR \_ não \_ inicializado**</dt> </dl>        | A função **createBlob** não foi chamada. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                         |
| <dl> <dt>**\_cadeia de blob NMERR \_ \_ inválida**</dt> </dl>         | A cadeia de caracteres não é terminada em nulo. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                                       |
| <dl> <dt>**NMERR \_ \_ gatilho ilegal**</dt> </dl>              | A parte do gatilho do BLOB de entrada está corrompida. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                        |
| <dl> <dt>**NMERR \_ \_ blob inválido**</dt> </dl>                 | O objeto especificado em *hInputBlob* não é um blob. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                      |
| <dl> <dt>**NMERR \_ \_ de \_ memória insuficiente**</dt> </dl>               | A memória necessária para executar essa operação não está disponível. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                              |
| <dl> <dt>**\_tempo limite de NMERR**</dt> </dl>                       | O tempo limite da solicitação foi atingido. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                                                               |
| <dl> <dt>**BLOB de upNMERR de \_ nível \_**</dt> </dl>                 | O número de versão do BLOB especificado em *hInputBlob* está incorreto. Esse erro é gerado pela chamada **IRTC:: Configure** .<br/>                                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Quando o método **Connect** é chamado, o NPP chama automaticamente o método **IRTC:: Configure** usando o blob fornecido pelo *hInputBlob*. Observe que todos os códigos de erro retornados pela chamada para **IRTC:: Configure** são passados de volta e retornados pela chamada **IRTC:: Connect** .

Esse método deve ser chamado antes que você possa iniciar a captura de quadros. Observe que quando você se conecta à rede usando esse método, você deve continuar a usar a interface **IRTC** para capturar quadros.

Ao chamar essa função, você deve especificar uma função de retorno de chamada de status ou quadro, mesmo que atue apenas como um espaço reservado.

O BLOB de entrada especificado por *hInputBlob* pode ser obtido chamando os métodos **GetNPPBlobFromUI**, **GetNPPBlobTable** e **SelectNPPBlobFromTable** .

O BLOB de erro retornado em *hErrorBlob* contém informações de erro que o desenvolvedor ou o aplicativo pode usar para solução de problemas. O BLOB de erro retornado por *hErrorBlob* contém entradas que monitor de rede não pôde entender ou localizar no blob de entrada especificado em *hInputBlob*. Por exemplo, se \_ a entrada de blob NMERR não \_ \_ \_ \_ existir for retornada, a entrada monitor de rede não poderá localizar é incluída no blob de erros retornado.



| Para obter informações sobre                          | Consulte                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------|
| Obtendo o BLOB de entrada que representa uma NIC | [Selecionando uma placa de interface de rede](selecting-a-network-interface-card.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC:: configurar](irtc-configure.md)
</dt> <dt>

[IRTC::D isconnect](irtc-disconnect.md)
</dt> <dt>

[IRTC:: iniciar](irtc-start.md)
</dt> </dl>

 

 




