---
title: Método GetObjectDataOnClearChannel
description: O método GetObjectDataOnClearChannel transfere um bloco de dados de objeto em um canal claro de volta para o Windows Media Gerenciador de Dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel Windows Media Gerenciador de Dispositivos
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770535"
---
# <a name="getobjectdataonclearchannel-method"></a>Método GetObjectDataOnClearChannel

O método **GetObjectDataOnClearChannel** transfere um bloco de dados de objeto em um canal claro de volta para o Windows Media Gerenciador de dispositivos.

Esse método é idêntico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , exceto que os dados retornados por esse método não são criptografados. Consequentemente, esse método é mais eficiente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDevice* 
</dt> <dd>

Ponteiro para o objeto do dispositivo.

</dd> <dt>

*pData* 
</dt> <dd>

Ponteiro para um buffer para receber dados.

</dd> <dt>

*pdwSize* 
</dt> <dd>

Ponteiro para um **DWORD** que contém o tamanho da transferência.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem sucedido, ele retornará S \_ OK. Se o método falhar, ele retornará um código de erro **HRESULT** .



| Código de retorno                                                                                                | Descrição                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ \_ \_ falha na verificação de Mac E WMDM \_**</dt> </dl> | O código de autenticação da mensagem não é válido.<br/>                                    |
| <dl> <dt>**WMDM \_ E não \_ à direita**</dt> </dl>           | O chamador não tem os direitos necessários para executar a operação solicitada.<br/> |
| <dl> <dt>**\_falso**</dt> </dl>                    | O método falhou. Terminar a interação com o provedor de conteúdo.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Um parâmetro é um ponteiro inválido ou **nulo** .<br/>                                   |
| <dl> <dt>**E \_ falha**</dt> </dl>                     | Ocorreu um erro não especificado.<br/>                                                   |



 

## <a name="remarks"></a>Comentários

Para transferir dados, o Windows Media Gerenciador de Dispositivos chama o método [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obter os dados do contêiner. Em seguida, **GetObjectDataOnClearChannel** é chamado para transferir blocos de dados de objeto do provedor de conteúdo para o Windows Media Gerenciador de dispositivos. Se S \_ OK for retornado com *pdwSize* definido como zero, o Windows Media Gerenciador de dispositivos não solicitará mais dados.

Esse método é idêntico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , exceto que os dados retornados por esse método não são criptografados. Consequentemente, esse método é mais eficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMSCP. idl</dt> </dl>    |
| Biblioteca<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**Interface ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





