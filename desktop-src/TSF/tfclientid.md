---
title: TfClientId (msctf. h)
description: O tipo de dados TfClientId é usado para identificar o cliente.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644493"
---
# <a name="tfclientid"></a>TfClientId

O tipo de dados **TfClientId** é usado para identificar o cliente.


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a>Comentários

No TSF, os aplicativos e serviços de texto são geralmente chamados de clientes. Cada cliente recebe um identificador exclusivo que ele usa para se identificar ao chamar vários métodos do Gerenciador de TSF. Esse identificador é do tipo **TfClientId** .

O tipo de dados **TfClientId** é fornecido pelo Gerenciador de TSF. Um aplicativo obtém um valor de **TfClientId** quando chama [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate). O valor de TfClientId para um serviço de texto é passado para o método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) . Qualquer objeto que não caiba nas categorias acima pode obter um identificador de cliente chamando [ITfClientId:: Getclientid](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                    |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                          |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITfClientId:: getclientid**](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[**ITfTextInputProcessor:: ativar**](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[**ITfThreadMgr:: ativar**](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





