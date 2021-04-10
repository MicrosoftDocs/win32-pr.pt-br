---
title: Função MpErrorMessageFormat (MpClient. h)
description: Retorna uma mensagem de erro formatada com base em um código de erro.
ms.assetid: C125FCE4-3BB0-4608-BBF3-E7FEF17D0807
keywords:
- Recursos do ambiente Windows herdado da função MpErrorMessageFormat
topic_type:
- apiref
api_name:
- MpErrorMessageFormat
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a3499b3be885b29135d22b470da4143cfb23ea6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919026"
---
# <a name="mperrormessageformat-function"></a>Função MpErrorMessageFormat

Retorna uma mensagem de erro formatada com base em um código de erro.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpErrorMessageFormat(
  _In_  MPHANDLE hMpHandle,
  _In_  HRESULT  hrError,
  _Out_ LPWSTR   *pwszErrorDesc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*hrError* \[ no\]
</dt> <dd>

Tipo: **HRESULT**

Um código de erro com base em **HRESULT**.

</dd> <dt>

*pwszErrorDesc* \[ fora\]
</dt> <dd>

Tipo: **LPWSTR \** _

Retorna uma mensagem de erro formatada com base em _hrError *. Essa cadeia de caracteres deve ser liberada usando [**MpFreeMemory**](mpfreememory.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha.

## <a name="remarks"></a>Comentários

Essa função é capaz de Formatar códigos de erro do sistema, além de códigos de erro específicos retornados pelas funções de proteção contra malware. Os códigos de erro **HRESULT** específicos das funções de proteção contra malware têm uma facilidade de 0x50. Abaixo está uma lista de um subconjunto dos códigos de erro específicos da proteção contra malware que podem ser retornados por várias funções de proteção contra malware. Usando a macro **HRESULT \_ do \_ \_ status do MP**, os códigos de erro a seguir podem ser convertidos em **HRESULT**. Consulte também [códigos de erro do mecanismo anti-malware do Forefront Client Security](https://support.microsoft.com/kb/939359) para obter uma lista de outros códigos de erro possíveis.



| Código do Erro                              | Descrição                                                                                                                 |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| ERRO \_ MP \_ noengine                     | Nenhum mecanismo é carregado no serviço antimalware para executar a operação solicitada.                                              |
| ERRO \_ MP \_ sem \_ memória                   | O mecanismo Antimalware encontrou uma situação sem memória.                                                               |
| ERRO \_ \_ ao remover MP \_ com falha               | Falha na operação de remoção de uma ameaça específica.                                                                              |
| \_ \_ falha na quarentena do MP de erro \_           | Falha na operação de quarentena para uma ameaça específica.                                                                          |
| ERRO \_ de \_ ameaça de MP \_ não \_ encontrada           | A ameaça específica não existe mais no sistema.                                                                         |
| ERRO \_ de \_ remoção de MP \_ sem \_ suporte       | Não há suporte para a operação de remoção de uma ameaça específica dentro do tipo de contêiner.                                          |
| ERRO \_ MP \_ Remover \_ contêiner imutável \_ | Devido à política do mecanismo, não há suporte para uma operação de remoção de uma ameaça específica dentro de um contêiner bloqueado. (Arquivos mortos de email). |
| ERRO \_ MP \_ BADDB \_ OLDENGINE             | A solicitação de atualização de assinatura forneceu arquivos de assinatura ou mecanismo mais antigos.                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[Códigos de erro do mecanismo anti-malware do Forefront Client Security](https://support.microsoft.com/kb/939359)
</dt> </dl>

 

 





