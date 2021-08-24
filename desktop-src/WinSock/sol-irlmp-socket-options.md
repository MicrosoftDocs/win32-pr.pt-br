---
description: A tabela a seguir descreve as opções de soquete SOL IRLMP que se aplicam a soquetes criados para a família de endereços AF IRDA (Associação de Dados \_ Desalorados) e o \_ IRLMP (InfraRed Link Management Protocol).
ms.assetid: 0457159d-8509-435c-8f57-752530d5df65
title: SOL_IRLMP de soquete (Af \_ irda.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2be68bc658cd7d55ff72a77b6ec87568c37d6d786d0a5e654e9276378b837c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860726"
---
# <a name="sol_irlmp-socket-options"></a>Opções de \_ soquete SOL IRLMP

A tabela a seguir descreve as opções de soquete **SOL \_ IRLMP** que se aplicam a soquetes criados para a família de endereços AF IRDA (Associação de Dados Desalorados) e o \_ IRLMP (InfraRed Link Management Protocol). Consulte as páginas de referência da função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

<dl> <dt><span id="SOL_IRLMP_Socket_Options"></span><span id="sol_irlmp_socket_options"></span><span id="SOL_IRLMP_SOCKET_OPTIONS"></span>**Opções de \_ soquete SOL IRLMP**</dt> <dd> <dl> <dt> 

| Opção                 | Obter | Definir | Tipo de aceitação     | Descrição                                                            |
|------------------------|-----|-----|-----------------|------------------------------------------------------------------------|
| MODO DE DESCOBERTA \_ \_ IRLMP |     |     |                 |                                                                        |
| IRLMP \_ ENUMDEVICES     | sim |     | **Devicelist**  | Retorna uma lista de IDs de dispositivo IrDA para dispositivos compatíveis com IR dentro do intervalo. |
| MODO EXCLUSIVO \_ \_ IRLMP |     |     | DWORD (booliana) | Define o soquete para ignorar a camada TinyTP para se comunicar diretamente com o IrLMP. |
| CONSULTA \_ IAS IRLMP \_      | sim |     | **CONSULTA \_ IAS**  | Consulta a IAS em um determinado serviço e nome de classe para seus atributos.      |
| IRLMP \_ IAS \_ SET        |     | sim | **IAS \_ SET**    | Define um valor de atributo para um determinado nome de classe e atributo em IAS. |
| MODO \_ IRLPT \_ IRLPT     |     | sim | DWORD (booliana) | Habilita a comunicação com impressoras com capacidade para IR.                        |
| PARÂMETROS IRLMP \_      |     |     |                 |                                                                        |
| IRLMP \_ SEND \_ PDU \_ LEN  | sim |     | DWORD           | Recupera o comprimento máximo de PDU necessário para usar IRLMP \_ 9WIRE \_ MODE.   |
| MODO SHARP \_ \_ IRLMP     |     | sim |                 |                                                                        |
| MODO \_ TINYTP IRLMP \_    |     | sim |                 |                                                                        |
| MODO IRLMP \_ \_ 9WIRE     | sim | sim | DWORD (booliana) | Coloca o soquete irDA no modo IrCOMM.                                 |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_SOL_IRLMP_options"></span><span id="windows_support_for_sol_irlmp_options"></span><span id="WINDOWS_SUPPORT_FOR_SOL_IRLMP_OPTIONS"></span>**Windows Suporte para opções \_ de IRLMP do SOL**</dt> <dd> <dl> <dt> 

| Opção                            | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows Eu, Windows 98 | Windows NT 4.0 |
|-----------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|------------------------|----------------|
| MODO DE DESCOBERTA \_ \_ IRLMP<br/> |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ ENUMDEVICES<br/>     | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODO EXCLUSIVO \_ \_ IRLMP<br/> |           |                     |               |                     |            |              |                        |                |
| CONSULTA \_ IAS IRLMP \_<br/>      | x         | x                   | x             | x                   | x          | x            | x                      |                |
| IRLMP \_ IAS \_ SET<br/>        | x         | x                   | x             | x                   | x          | x            | x                      |                |
| MODO \_ IRLPT \_ IRLPT<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |
| PARÂMETROS IRLMP \_<br/>      |           |                     |               |                     |            |              | x                      |                |
| IRLMP \_ SEND \_ PDU \_ LEN<br/>  | x         | x                   | x             | x                   | x          | x            |                        |                |
| MODO SHARP \_ \_ IRLMP<br/>     |           |                     |               |                     |            |              |                        |                |
| \_modo de TINYTP IRLMP \_<br/>    |           |                     |               |                     |            |              | x                      |                |
| \_Modo de 9WIRE IRLMP \_<br/>     | x         | x                   | x             | x                   | x          | x            |                        |                |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

As opções de soquete **sol \_ IRLMP** e as estruturas usadas por essas opções de soquete são definidas no arquivo de cabeçalho *\_ IrDA. h de AF* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>\_IrDA. h de AF</dt> </dl> |



 

 




