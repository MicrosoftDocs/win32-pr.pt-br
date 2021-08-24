---
title: Método ReactivateServerAutomatic da classe Win32_TSLicenseServer
description: Reativa o servidor de licença Área de Trabalho Remota usando uma conexão automática com a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ReactivateServerAutomatic
- Método ReactivateServerAutomatic Serviços de Área de Trabalho Remota, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Serviços de Área de Trabalho Remota, método ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4e822c441410ae3757f7cdb0a4a714b435facbb20e171646c889e2ea53ec82b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866036"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Método ReactivateServerAutomatic da classe Win32 \_ TSLicenseServer

Reativa o servidor de licença Área de Trabalho Remota usando uma conexão automática com a Internet.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Motivo* \[ no\]
</dt> <dd>

Motivo da ativação. Pode ser um dos seguintes valores.

<dt>

0
</dt> <dd>

O servidor foi reimplantado.

</dd> <dt>

1
</dt> <dd>

O certificado foi corrompido.

</dd> <dt>

2
</dt> <dd>

A chave privada foi comprometida.

</dd> <dt>

3
</dt> <dd>

A chave de ativação expirou.

</dd> <dt>

4
</dt> <dd>

O servidor foi atualizado.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ fora\]
</dt> <dd>

O status de ativação retornado pode ser um dos valores a seguir.

<dt>

0
</dt> <dd>

O servidor de licença Área de Trabalho Remota está ativado.

</dd> <dt>

1
</dt> <dd>

O servidor de licença Área de Trabalho Remota não está ativado.

</dd> <dt>

2
</dt> <dd>

Ocorreu um erro desconhecido. Não é conhecido se o servidor de licença Área de Trabalho Remota está ativado.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método tiver sucesso, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

