---
description: Enumera todos os certificados no sistema que correspondem aos critérios indicados e retorna uma lista de impressões digitais.
ms.assetid: 69522afe-9870-4ae9-8c69-cf8787913615
title: Método FindValidCertificates da classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.FindValidCertificates
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 69612d860284f6a47dfa38c2aafc3e73f209c796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297100"
---
# <a name="findvalidcertificates-method-of-the-win32_encryptablevolume-class"></a>Método FindValidCertificates da classe Win32 \_ EncryptableVolume

O método **FindValidCertificates** da classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) enumera todos os certificados no sistema que correspondem aos critérios indicados e retorna uma lista de impressões digitais. A lista retornada contém apenas certificados com um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) válido. O OID pode ser o padrão ou pode ser especificado no Política de Grupo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 FindValidCertificates(
  [out] string CertificateThumbprint[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*CertificateThumbprint* \[ fora\]
</dt> <dd>

Tipo: **cadeia \[ \] de caracteres**

Uma matriz de cadeias de caracteres que contém a lista de certificados válidos.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Esse método retornará um dos códigos a seguir ou outro código de erro se ele falhar.



| Código/valor de retorno                                                                                                                                                                           | Descrição                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl>                                           | O método foi bem-sucedido.<br/>                |
| <dl> <dt>**FVE \_ E \_ \_ \_ OID do BITLOCKER**</dt> <dt>2150695022 (0x8031006E)</dt> inválido </dl> | O OID do BitLocker disponível não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows 7 Enterprise, Windows 7 Ultimate \[\]<br/>                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                 |
| Namespace<br/>                | \\MicrosoftVolumeEncryption de \\ segurança \\ cimv2 raiz<br/>                                             |
| MOF<br/>                      | <dl> <dt>Win32 \_ encryptablevolume. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_EncryptableVolume Win32**](win32-encryptablevolume.md)
</dt> </dl>

 

 
