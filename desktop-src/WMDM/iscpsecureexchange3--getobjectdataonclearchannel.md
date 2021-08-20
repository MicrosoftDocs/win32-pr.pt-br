---
title: Método GetObjectDataOnClearChannel
description: O método GetObjectDataOnClearChannel transfere um bloco de dados de objeto em um canal não limpo para Windows Media Gerenciador de Dispositivos.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Método GetObjectDataOnClearChannel windows Media Gerenciador de Dispositivos
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
ms.openlocfilehash: c10e09697653c2ef1235ae9a3ea3a93a45437d1cf45a1f4de72ec99b0812b9b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619866"
---
# <a name="getobjectdataonclearchannel-method"></a>Método GetObjectDataOnClearChannel

O **método GetObjectDataOnClearChannel** transfere um bloco de dados de objeto em um canal não limpo para Windows Media Gerenciador de Dispositivos.

Esse método é idêntico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) exceto que os dados retornados por esse método não são criptografados. Consequentemente, esse método é mais eficiente.

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

*Pdata* 
</dt> <dd>

Ponteiro para um buffer para receber dados.

</dd> <dt>

*Pdwsize* 
</dt> <dd>

Ponteiro para um **DWORD** que contém o tamanho da transferência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se o método falhar, ele retornará um **código de erro HRESULT.**



| Código de retorno                                                                                                | Descrição                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**FALHA NA VERIFICAÇÃO DO WMDM \_ E \_ \_ MAC \_**</dt> </dl> | O código de autenticação de mensagem não é válido.<br/>                                    |
| <dl> <dt>**WMDM \_ E \_ NORIGHTS**</dt> </dl>           | O chamador não tem os direitos necessários para executar a operação solicitada.<br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                    | O método falhou. Encerrar a interação com o provedor de conteúdo.<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Um parâmetro é um ponteiro inválido **ou NULL.**<br/>                                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Ocorreu um erro não especificado.<br/>                                                   |



 

## <a name="remarks"></a>Comentários

Para transferir dados, Windows Media Gerenciador de Dispositivos chama o [método TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) para obter os dados do contêiner. **GetObjectDataOnClearChannel** é chamado para transferir blocos de dados de objeto do provedor de conteúdo para Windows Mídia Gerenciador de Dispositivos. Se O \_ S OK for retornado com *pdwSize* definido como zero, Windows Mídia Gerenciador de Dispositivos não solicitará mais dados.

Esse método é idêntico a [**ISCPSecureExchange::ObjectData,**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) exceto que os dados retornados por esse método não são criptografados. Consequentemente, esse método é mais eficiente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>WMSCP.idl</dt> </dl>    |
| Biblioteca<br/> | <dl> <dt>Mssachlp.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[**ISCPSecureExchange3 Interface**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





