---
description: O CAPICOM não habilita a verificação de revogação de certificado por padrão.
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: Verificando o status de revogação do certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170779"
---
# <a name="checking-certificate-revocation-status"></a>Verificando o status de revogação do certificado

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

O CAPICOM não habilita a verificação de revogação de certificado por padrão. No entanto, a verificação de revogação de certificado pode ser habilitada programaticamente para um certificado específico por meio da propriedade **IsValid. CheckFlag** de um objeto de certificado. Depois que o valor apropriado de **CheckFlag** tiver sido definido, acessar a propriedade **IsValid. Result** do objeto de certificado ou criar o caminho de verificação do certificado usando um método de criação do objeto de cadeia forçará a verificação de revogação.

No exemplo a seguir, o certificado foi instanciado como um certificado capicor válido.


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



O anterior se aplica a um certificado individual, independentemente de como ele foi obtido. Executar a verificação de revogação nos certificados em um objeto [**SignedData**](signeddata.md) não é diferente porque o método [**Verify**](signeddata-verify.md) do objeto **SignedData** não pode ser usado para essa finalidade porque a habilitação de CAPICOM a \_ \_ assinatura e o \_ \_ certificado não causam a verificação da CRL.

Em vez disso, o **CheckFlag** deve ser definido para o certificado de cada signatário. Considere o exemplo a seguir, em que sData foi instanciado como um objeto [**SignedData**](signeddata.md) de CAPICOM válido.


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



O exemplo adicional é o loop sobre todos os certificados no objeto [**SignedData**](signeddata.md) .

 

 



