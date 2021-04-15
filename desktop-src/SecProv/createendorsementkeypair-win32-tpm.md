---
description: Cria um par de chaves de endosso de 2048 bits no TPM.
ms.assetid: 393f0264-d1e9-4a08-bdaa-475b32d93e05
title: Método CreateEndorsementKeyPair da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.CreateEndorsementKeyPair
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5839dc009d8af420a91f2e7c925f2cac5567d2a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501535"
---
# <a name="createendorsementkeypair-method-of-the-win32_tpm-class"></a>Método CreateEndorsementKeyPair da classe Win32 \_ TPM

O método **CreateEndorsementKeyPair** da classe [**Win32 \_ TPM**](win32-tpm.md) cria um par de chaves de endosso de 2048 bits no TPM. O par de chaves de endosso deve estar disponível para que o método [**TakeOwnership**](takeownership-win32-tpm.md) seja executado com êxito. Você pode usar o método [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md) para detectar se a chave de endosso já existe no TPM.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateEndorsementKeyPair();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

A tabela a seguir lista alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                                                  | Descrição                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                  | O método foi bem-sucedido.<br/>                          |
| <dl> <dt> **TPM \_ E \_ desabilitou \_ cmd**</dt> <dt>2150105096 (0x80280008)</dt> </dl> | Um par de chaves de endosso já existe neste TPM.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
